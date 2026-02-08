# Interview Questions - Fullstack Engineer

## Java/Spring Boot Question

**File:** `InventoryService.java`

### Task
Implement the `decrementStock()` method in `InventoryService` and the endpoint in `InventoryController`.

### Requirements

#### 1. InventoryService.decrementStock()
- Find product by ID
- Check if sufficient stock exists
- Decrement stock atomically
- Return updated product
- Throw appropriate exceptions for invalid cases

#### 2. InventoryController.decrementStock()
- Validate quantity > 0
- Call `inventoryService.decrementStockWithRetry()`
- Return proper HTTP responses:
  - `400` for validation errors (quantity <= 0, insufficient stock)
  - `404` if product not found
  - `200` with product body on success

### API
```
POST /api/products/{id}/decrement
Body: { "quantity": 1 }
Response: { "id": 1, "name": "Product", "stock": 99, "version": 1 }
```

### Hints
- Use `@Version` for optimistic locking
- Retry logic is already implemented in `decrementStockWithRetry()`
- Use `@Transactional` with `REPEATABLE_READ` isolation

---

## Angular Question

**File:** `user-list.component.ts`

### Task
Implement `onSearchInput()`, `loadUsers()`, and `ngOnDestroy()` in `UserListComponent`.

### Requirements

#### 1. onSearchInput()
- Debounce input by 300ms
- Reset to page 1 when search changes
- Avoid redundant API calls for same search query

#### 2. loadUsers()
- Fetch users from `/api/users` with pagination and search
- Set loading state before API call
- Handle errors with try/catch
- Update `users` and `total` on success
- Clear loading state in finally block

#### 3. ngOnDestroy()
- Clear debounce timer to prevent memory leaks
- Set destroyed flag to prevent state updates after destroy

### API
```
GET /api/users?page=1&limit=20&search=query
Response: { "users": [...], "total": 100, "page": 1, "limit": 20 }
```

### Hints
- Use `setTimeout` for debouncing
- Use `clearTimeout` to cancel debounce
- Use `URLSearchParams` to build query string

---

## Evaluation Criteria

| Criterion | Java | Angular |
|-----------|------|---------|
| Async/await patterns | ✅ | ✅ |
| Error handling | ✅ | ✅ |
| Proper validation | ✅ | ✅ |
| Memory management | N/A | ✅ |
| Clean, readable code | ✅ | ✅ |
