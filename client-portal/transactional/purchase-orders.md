# Purchase Orders

Purchase Orders (POs) are used to notify the 3PL of incoming stock. Navigate to **Transactional → Purchase Orders** to access this section.

Orders can be created **manually** or loaded in bulk via **import**.

> 📷 Screenshot: Purchase Orders list screen with New and Import buttons.

---

## Manual Creation

> 📷 Video reference: Step-by-step walkthrough for creating a Purchase Order manually (`Orden de Compra Manual.mp4`).

### Step by Step

1. Click **New**. A window will appear — select the **vendor** and the **warehouse**.

> 📷 Screenshot: New PO window with vendor and warehouse selectors.

2. Add products **line by line**. Search by SKU or description to locate each item quickly.
3. Once all products have been added, **release the order** to submit it to the 3PL.

> 📷 Screenshot: PO detail screen showing product lines and the Release button.

### After Release

- The order appears in the portal with the status **"Unreceived"**, meaning it has not yet been physically processed by the warehouse.
- While in **Unreceived** status, the order can still be **deleted**, as it has not yet been worked by the 3PL.
- The order will appear in **P4 Warehouse** with the same order number shown in the Client Portal (e.g. `PO-0000041`).

{% hint style="danger" %}
Once the 3PL begins receiving the order, it can no longer be deleted or modified. From that point, the client can only view the order's status.
{% endhint %}

> 📷 Screenshot: PO list showing an order in Unreceived status.

---

## Import (Bulk Creation)

> 📷 Video reference: Step-by-step walkthrough for creating Purchase Orders by bulk import (`Orden de Compra creada por importación.mp4`).

### Template Requirements

You must use the system's official import template. The template contains column headers in English that **must not be translated, renamed, or modified** in any way.

The required fields are:

| Field | Description |
|---|---|
| `VendorCode` | Vendor code |
| `OrderGroup` | Order grouping identifier |
| `Warehouse` | Warehouse |
| `ReferenceNumber` | Reference number |
| `Comments` | Comments |
| `RequiredDate` | Required date |
| `Sku` | Product SKU |
| `Quantity` | Quantity |
| `Packsize` | Pack size — only complete if the product has a pack size; otherwise leave blank |

### The OrderGroup Field

The `OrderGroup` field controls how rows are grouped into orders:

- All rows with the **same** `OrderGroup` value are treated as a single order.
- When the value **changes**, the system creates a new order.
- Use any identifier (e.g. `order1`, `order2`, `A1`, `A2`) as long as the grouping is consistent.

**Example:**
- Rows with `orden1` → grouped into one order
- Rows with `orden2` → grouped into a separate order

### Step by Step

1. Go to **Transactional → Purchase Orders** and click **Import** (top right).
2. The system will immediately open a file browser — select your Excel file.

> 📷 Screenshot: File browser opened for selecting the import file.

3. After selecting the file, a confirmation message will appear — validate the import.

> 📷 Screenshot: Import confirmation dialog.

4. Imported orders are created in **Draft** status. Open each order and **release** it for the 3PL to see it.

> 📷 Screenshot: PO list showing imported orders in Draft status.

{% hint style="warning" %}
Imported orders remain in Draft until manually released. They are not visible to the 3PL until released.
{% endhint %}

---

**Next:** [Pick Tickets](pick-tickets.md) · **Related:** [Vendors](../master-data/vendors.md)
