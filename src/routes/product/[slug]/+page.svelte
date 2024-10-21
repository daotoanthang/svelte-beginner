<script context="module">
  // Đây là hàm `load` để lấy dữ liệu liên quan đến `slug`
  // @ts-ignore
  export async function load({ params }) {
    const { slug } = params;

    // Giả sử bạn có API để lấy thông tin sản phẩm dựa trên slug
    console.log(slug);
  }
</script>

<script>
  export let product = {
    name: "iphone",
    description: "iphone",
    price: "100$",
  };
</script>

<h1>{product.name}</h1>
<p>{product.description}</p>
<p>Price: ${product.price}</p>
