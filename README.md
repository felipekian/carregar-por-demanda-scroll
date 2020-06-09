# Carregar Dados Por Demanda

```
cont_scroll_page_end = 1

function getProxDatas() {
    $.ajax({
        type: '',
        url: '',
        data: {
            'scroll_count': cont_scroll_page_end
        },
        dataType: 'json',
        success: function (response) {
            if (response.status == 1) {
                //render
            } else {
                //falha
            }
        }
    });
}

$(window).scroll(function () {
    if ($(this).scrollTop() + $(this).height() >= $(document).height() * 0.9) {
        cont_scroll_page_end++;
        getProxDatas();
    }
});
```
