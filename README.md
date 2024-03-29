## В данном проекте мною проводился анализ e-commerce магазина
### Работа выполнена на Python с использованием Jupyter Notebook.

---

## В ходе проекта решались следующие задачи:
- найти сколько пользователей, которые совершили покупку только один раз;
- выяснить сколько заказов в месяц в среднем не доставляется по разным причинам;
- по каждому товару определить, в какой день недели товар чаще всего покупается;
- определить сколько у каждого из пользователей в среднем покупок в неделю (по месяцам);
- провести когортный анализ пользователей, выявить когорту с самым высоким retention на 3й месяц;
- построить RFM-сегментацию пользователей, чтобы качественно оценить аудиторию.

---

## Описание данных:
- olist_customers_datase.csv — таблица с уникальными идентификаторами пользователей:
  - customer_id — позаказный идентификатор пользователя
  - customer_unique_id — уникальный идентификатор пользователя
  - customer_zip_code_prefix — почтовый индекс пользователя
  - customer_city — город доставки пользователя
  - customer_state — штат доставки пользователя
  
- olist_orders_dataset.csv — таблица заказов:
  - order_id — уникальный идентификатор заказа (номер чека)
  - customer_id — позаказный идентификатор пользователя
  - order_status — статус заказа:
    - created — создан
    - approved — подтверждён
    - invoiced — выставлен счёт
    - processing — в процессе сборки заказа
    - shipped — отгружен со склада
    - delivered — доставлен пользователю
    - unavailable — недоступен
    - canceled — отменён
    - order_purchase_timestamp — время создания заказа

- order_approved_at — время подтверждения оплаты заказа:
  - order_delivered_carrier_date — время передачи заказа в логистическую службу
  - order_delivered_customer_date — время доставки заказа
  - order_estimated_delivery_date — обещанная дата доставки
  - olist_order_items_dataset.csv — товарные позиции, входящие в заказы
  - order_id — уникальный идентификатор заказа (номер чека)
  - order_item_id — идентификатор товара внутри одного заказа (не содержит информацию о количестве товаров)
  - product_id — уникальный идентефикатор товара (аналог штрихкода)
  - seller_id — уникальный идентефикатор производителя товара
  - shipping_limit_date — максимальная дата доставки продавцом для передачи заказа партнеру по логистике
  - price — цена за единицу товара
  - freight_value — вес товара
