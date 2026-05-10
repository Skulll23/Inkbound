# Graph Report - /private/tmp/Inkbound-audit  (2026-05-11)

## Corpus Check
- 8 files · ~873,677 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 175 nodes · 414 edges · 11 communities detected
- Extraction: 71% EXTRACTED · 29% INFERRED · 0% AMBIGUOUS · INFERRED: 122 edges (avg confidence: 0.8)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- [[_COMMUNITY_Community 0|Community 0]]
- [[_COMMUNITY_Community 1|Community 1]]
- [[_COMMUNITY_Community 2|Community 2]]
- [[_COMMUNITY_Community 3|Community 3]]
- [[_COMMUNITY_Community 4|Community 4]]
- [[_COMMUNITY_Community 5|Community 5]]
- [[_COMMUNITY_Community 6|Community 6]]
- [[_COMMUNITY_Community 7|Community 7]]
- [[_COMMUNITY_Community 8|Community 8]]
- [[_COMMUNITY_Community 9|Community 9]]
- [[_COMMUNITY_Community 10|Community 10]]

## God Nodes (most connected - your core abstractions)
1. `apiFetch()` - 35 edges
2. `showToast()` - 19 edges
3. `loadProducts()` - 17 edges
4. `emitAppSnapshot()` - 13 edges
5. `handleLogin()` - 13 edges
6. `openAdminPanel()` - 13 edges
7. `renderSkeletons()` - 10 edges
8. `renderCart()` - 10 edges
9. `handleRegister()` - 10 edges
10. `submitCheckout()` - 9 edges

## Surprising Connections (you probably didn't know these)
- `renderViewControls()` --calls--> `setViewMode()`  [INFERRED]
  /private/tmp/Inkbound-audit/frontend/js/ui.js → /private/tmp/Inkbound-audit/frontend/js/app.js
- `showToast()` --calls--> `handleAddToCart()`  [INFERRED]
  /private/tmp/Inkbound-audit/frontend/js/ui.js → /private/tmp/Inkbound-audit/frontend/js/app.js
- `showToast()` --calls--> `handleWishlistToggle()`  [INFERRED]
  /private/tmp/Inkbound-audit/frontend/js/ui.js → /private/tmp/Inkbound-audit/frontend/js/app.js
- `showToast()` --calls--> `handleSubmitReview()`  [INFERRED]
  /private/tmp/Inkbound-audit/frontend/js/ui.js → /private/tmp/Inkbound-audit/frontend/js/app.js
- `showToast()` --calls--> `handleDeleteReview()`  [INFERRED]
  /private/tmp/Inkbound-audit/frontend/js/ui.js → /private/tmp/Inkbound-audit/frontend/js/app.js

## Communities

### Community 0 - "Community 0"
Cohesion: 0.11
Nodes (29): applyCategoryBySlug(), applyCollection(), applySavedFilterCollection(), clearAdvancedFilters(), clearSearch(), closeAdminPanel(), closeAutocomplete(), closeCommandPalette() (+21 more)

### Community 1 - "Community 1"
Cohesion: 0.16
Nodes (26): addToCart(), addToWishlist(), apiCreateAdminProduct(), apiFetch(), apiGetAdminProducts(), apiGetAdminReviews(), apiGetAdminUsers(), apiGetAllOrders() (+18 more)

### Community 2 - "Community 2"
Cohesion: 0.12
Nodes (16): getStoredUser(), calculateCheckoutTotals(), openCheckout(), authorBio(), categoryTotals(), cleanImageUrl(), escHtml(), monthlySales() (+8 more)

### Community 3 - "Community 3"
Cohesion: 0.15
Nodes (21): apiDeleteAdminProduct(), apiUpdateOrderStatus(), clearCart(), placeOrder(), removeCartItem(), removeStoredUser(), removeToken(), updateCartItem() (+13 more)

### Community 4 - "Community 4"
Cohesion: 0.16
Nodes (19): apiLogin(), apiRegister(), fetchCart(), fetchWishlistIds(), setStoredUser(), setToken(), cartProductIds(), closeAuthModal() (+11 more)

### Community 5 - "Community 5"
Cohesion: 0.16
Nodes (7): connectMongo(), ensureMongoSeed(), getCartResponse(), getCollections(), getTokenUser(), requireUser(), userFromDb()

### Community 6 - "Community 6"
Cohesion: 0.18
Nodes (13): deleteReview(), fetchReviews(), fetchSimilar(), submitReview(), getCatalogHighlights(), getRecentlyViewed(), handleDeleteReview(), handleSubmitReview() (+5 more)

### Community 7 - "Community 7"
Cohesion: 0.22
Nodes (9): fetchOrders(), fetchWishlist(), openAuthModal(), openOrders(), openWishlist(), switchAuthView(), renderAuthModal(), renderOrderHistory() (+1 more)

### Community 8 - "Community 8"
Cohesion: 0.5
Nodes (2): formatMoney(), ReactAssignmentDashboard()

### Community 9 - "Community 9"
Cohesion: 1.0
Nodes (0):

### Community 10 - "Community 10"
Cohesion: 1.0
Nodes (0):

## Knowledge Gaps
- **Thin community `Community 9`** (1 nodes): `catalog.js`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 10`** (1 nodes): `server.js`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `openAdminPanel()` connect `Community 1` to `Community 0`, `Community 2`, `Community 3`?**
  _High betweenness centrality (0.049) - this node is a cross-community bridge._
- **Why does `showToast()` connect `Community 3` to `Community 0`, `Community 1`, `Community 2`, `Community 4`, `Community 6`?**
  _High betweenness centrality (0.047) - this node is a cross-community bridge._
- **Why does `apiFetch()` connect `Community 1` to `Community 3`, `Community 4`, `Community 6`, `Community 7`?**
  _High betweenness centrality (0.046) - this node is a cross-community bridge._
- **Are the 18 inferred relationships involving `showToast()` (e.g. with `handleAddToCart()` and `handleUpdateQty()`) actually correct?**
  _`showToast()` has 18 INFERRED edges - model-reasoned connections that need verification._
- **Are the 2 inferred relationships involving `loadProducts()` (e.g. with `fetchProducts()` and `renderProducts()`) actually correct?**
  _`loadProducts()` has 2 INFERRED edges - model-reasoned connections that need verification._
- **Are the 6 inferred relationships involving `handleLogin()` (e.g. with `apiLogin()` and `setToken()`) actually correct?**
  _`handleLogin()` has 6 INFERRED edges - model-reasoned connections that need verification._
- **Should `Community 0` be split into smaller, more focused modules?**
  _Cohesion score 0.11 - nodes in this community are weakly interconnected._