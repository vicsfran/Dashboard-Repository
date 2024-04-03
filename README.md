# PP_Practice_PowerBI

### Projects developed for application of ideas in the creation of data visualization panels.

#### Dashboard Commercial: https://app.powerbi.com/view?r=eyJrIjoiYzk5NDYzYzUtOWQyZi00OWIyLWE5OTQtYTMyOTAzNWE5NTA4IiwidCI6IjgyYTU4NjE2LTY4ZDYtNDA1MS05Y2E5LWIyY2U2YmE1MjEzNCJ9

#### Dashboard Logistics: https://app.powerbi.com/view?r=eyJrIjoiMTQ0ZDhlY2MtZTM1Ny00NThmLTg2NzYtM2I3MmFiODgyMDU4IiwidCI6IjgyYTU4NjE2LTY4ZDYtNDA1MS05Y2E5LWIyY2U2YmE1MjEzNCJ9

Metrics by Logistics and Linguage DAX used:

- Placed Orders = count of orders placed.7
      
- Delivered Orders = count of orders, exclude those with blank delivery data.
      
      DAX: Volume expedido = SUM(fNotasFiscais[Volumes])

-  Open Orders = accumulated value of the difference between orders placed and delivered over the period.

-  Order Fill Rate (OFR) = average of days between the order date and the CTE issuance date. Represents the time that the operation takes to pick an order, including all activities — from the recipient of the purchase order to shipment.

-  Order Cycle Time (OCT) = average days between order and delivery date. It aims to measure how long the company takes to make a delivery, from dispatch to arrival at the destination, that is, the overall efficiency of the operation.
  
       DAX: Tempo Médio Entrega = AVERAGE(fNotasFiscais[PrazoEntrega])

-  On Time = number of orders delivered with a delivery date less than or equal to the expected date. Measures order timeliness.
  
       DAX: Qtd On time = CALCULATE([Notas fiscais], fNotasFiscais[On Time Delivery] = "On Time")

-  % On Time = proportion between orders On Time in relation to the total orders delivered.

       DAX:  % On time = DIVIDE([Qtd On time], [Notas fiscais])

-  In Full = number of orders with zero occurrences of returns. Evaluates compliance with specifications agreed with the customer, such as quality, dimensions, quantity and price.
  
       DAX: Qtd In full = CALCULATE([Notas fiscais], fNotasFiscais[In Full Delivery] = "In full")

-  % In Full = proportion between In Full orders in relation to the total number of delivered orders.
      
       DAX: % In full = DIVIDE([Qtd In full], [Notas fiscais])

-  % OTIF = % On Time and % In Full multiplication. This segmentation makes it possible to identify whether the origin of the problem is in the delivery or in the     expedition. Low On Time means that there is a need to review the transport process or improve negotiation of expected delivery data. On the other hand, a low In Full may indicate problems in processing, sorting, packaging, checking or dispatching the products.
  
       DAX: OTIF = [% In full] * [% On time]

____________________________________________________________________________________________________________________________________

#### Dashboard Sales: https://app.powerbi.com/view?r=eyJrIjoiMDE3NWY4OTYtOTY0Yy00N2YzLWEyNmMtOWY2ODFhMzllMGJlIiwidCI6IjgyYTU4NjE2LTY4ZDYtNDA1MS05Y2E5LWIyY2U2YmE1MjEzNCJ9

#### Dashboard NPS: https://app.powerbi.com/view?r=eyJrIjoiNDhlZTg2MDQtMGMzZi00ZDJmLTkxOGYtZDY2ZGZlZTVhY2MwIiwidCI6IjgyYTU4NjE2LTY4ZDYtNDA1MS05Y2E5LWIyY2U2YmE1MjEzNCJ9


