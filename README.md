# Detect human parts (PARTNet)
[![Generic badge](https://img.shields.io/badge/Contributions-Welcome-brightgreen.svg)]()
[![Status badge](https://img.shields.io/badge/status-in%20progress-green.svg)]()
[![Type badge](https://img.shields.io/badge/type-compact-blueviolet.svg)]()

<p align="center">
  <img src="banner.png" width="100%"/>
</p>

<img src="https://img.shields.io/badge/-nose-lightgrey.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAQAAADZc7J/AAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAAmJLR0QAAKqNIzIAAAAJcEhZcwAADsQAAA7EAZUrDhsAAAAHdElNRQfjBhQAGRSN5YuBAAABlUlEQVRIx6XTz4tNcRjH8deduWakMRmElZowdfMjP0YopYQ/YJbYsJKyULY2ktIsx4KFjWwmNmOsiC5lMbsppBRywzRqhFnQcM9jMdc057qj2/d8Vud5ns959/l+n3NYWvs8NaiAbggvdacDer0XLhXJcEzmlwNFENeFKRvTAV2qwgu96Yh13gljyumIiq/CeJF9HPJduG95OmLQjFDVk47YY0Z4UuQ6d5gWJqxOR1R8Eib1pSP6vRUmrCyCqAmj6QC2+yYMzRedCYDPyg7rcAc6Gs2SYVvaRnxENv/4F7DfBVWlNgEDDcgiwFGMiZb25r13GkI1D9iE503Gbqc98sN4U/+MAR88zDfvCicW1SWn1IQQHuecx/1s8oJh4eZCtdczIbx21vpcpisyYeTfc26TqTunbKvbMuGL87pynoNeCZnLrS/7YiNwCHNGrMlNe1xTF944svRyTqoJs26pNE3WmhTmXLXCf1XS1zLeqDBtp0St8ls9/XU2CLMLX0ySpoRdrUft/Y0Vuy1zLz3BZg/0tx79ASZmdQmoPDnPAAAAJXRFWHRkYXRlOmNyZWF0ZQAyMDE5LTA2LTE5VDIyOjI1OjIwKzAyOjAwxEgfFAAAACV0RVh0ZGF0ZTptb2RpZnkAMjAxOS0wNi0xOVQyMjoyNToyMCswMjowMLUVp6gAAAAZdEVYdFNvZnR3YXJlAHd3dy5pbmtzY2FwZS5vcmeb7jwaAAAAAElFTkSuQmCC"> <img src="https://img.shields.io/badge/-mouth-lightgrey.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAQAAADZc7J/AAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAAmJLR0QAAKqNIzIAAAAJcEhZcwAADsQAAA7EAZUrDhsAAAAHdElNRQfjBhQAHi2doZVOAAAB/UlEQVRIx+3TXWgNYBwG8N/OsSWznZbZlqhdrCWxCzfSpE3JxZZCUSRlbhS7UYu4cutjsQucNBRKKaRdyZJIzdfK5+SjNlsz2sFs1M7Z68I2djqG2+V5b96e//s8/f/Pv5f/mIKIWKNFry5nlI+zZU7r9E6LtaKTyas8FHRo0qzfV7tFRTUYktCsyXNBu6rM4pmOG9FtvQgodFbwzFPBeYUgyzpdRpyQly5fpEPSUfkT2FrXtVo9gcvTKOmFil/JzQZ1W/bXSS3x0qAtY7EdFtxU8k9h57sgOCI6TVyduB2iChQqUmyOEvPMVSAmJiJhyEfderzVp1evIQO2+6BeQZZPaXOT0ich4aOEhCBfTExMgRIz0t72sE3wyANBcNsK80ybpPVZlrkpCO7okbQKDhpWq9pVI/rFVcvOKJ6hxjmDUi6ptEfQMBbjJV9UYr5G7wUDWuxSrUS2HHOttFerb4J3DijHRiknf3rnuufz6BpzrBH3Wkg7LxyzerS3DZKu/bhnjVoUu67UJlfGTUstVCpPMOC1JzrHKzs1uqXWl4kTFmmTsm/SCMkTF1yWm6k43SlBu6W/EWdZq8uw/aO/JSNqvBHcsM7MCfxsdR4L7luc7pqOXFvVK5PU5pX3IoosUCHirkMuSv3J4MdiK62w3BzFUvp0anVNu/+YqvgOklmmrhmavDcAAAAldEVYdGRhdGU6Y3JlYXRlADIwMTktMDYtMTlUMjI6MzA6NDUrMDI6MDB3uC2wAAAAJXRFWHRkYXRlOm1vZGlmeQAyMDE5LTA2LTE5VDIyOjMwOjQ1KzAyOjAwBuWVDAAAABl0RVh0U29mdHdhcmUAd3d3Lmlua3NjYXBlLm9yZ5vuPBoAAAAASUVORK5CYII="> <img src="https://img.shields.io/badge/-eye-lightgrey.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAQAAADZc7J/AAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAAmJLR0QAAKqNIzIAAAAJcEhZcwAADsQAAA7EAZUrDhsAAAAHdElNRQfjBhQAIRMEHqLZAAACAElEQVRIx+3UO09UURQF4I+JaCjEoBDRxAcFpZFEbZSIjygYjaVRS1+gv8CCWkV/BcgfQNHEQqMWBoh2CIU6hRgjCpgwCeOYIduC683M8BC1Zd3m7OystfdeZ9/DGv4bVStmt6vDd5//VrbWNYNmRPLNeOiq2tWRN7kjl1LnzKXnWbf/JFLluq9CeK/HQfWg3iE9PghhUufyYzd4LIRR52TALh067AIZ540JYTARrsABn4QfbloHjhpJmx/WBtbpVhAm7Kukt8sJ7+xJ4hvmhaJRo4pCUVeSaZEVck6U0s/6KTxVl8RHzQu9toJGfULR4SRb74VQcPo3/Zi8MGBDKjgi9JZ1eF8YSqMaj4S8I9BkSnhWQm8SihrLBLYpisROWO+JMKOZN8JrG8v8CKOLTH4rnCyJaxeYGbGa7VoS8bvhbxUj7F52hJ0VI0xrXvA8LzxUk6aHhb4ygX7hVYmJg8Jcei/OKAjPbUniNkXhvm1J9X6hqDW9xpdCwanSCifkhKyWJO5K1mfMWHK6lmT2ygqzjldast+EUNCtGhw2lK7yq6R6dbLKHxev8kJrg0IYdyH5mXZq124HyLhoXAgP0lEXoUqnSSFk3dWqATRodU9WCF9c+cMrptZts2nzefmSB+VW2cKtgI0uGzCVUqcMuLQ0eeV2Gm3GtMnV1V3DP+IXaRrY+0Yy27IAAAAldEVYdGRhdGU6Y3JlYXRlADIwMTktMDYtMTlUMjI6MzM6MTkrMDI6MDATz/KjAAAAJXRFWHRkYXRlOm1vZGlmeQAyMDE5LTA2LTE5VDIyOjMzOjE5KzAyOjAwYpJKHwAAABl0RVh0U29mdHdhcmUAd3d3Lmlua3NjYXBlLm9yZ5vuPBoAAAAASUVORK5CYII="> <img src="https://img.shields.io/badge/-eyebrow-lightgrey.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAQAAADZc7J/AAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAAmJLR0QAAKqNIzIAAAAJcEhZcwAADdcAAA3XAUIom3gAAAAHdElNRQfjBhQAIwpSQ2ibAAACeElEQVRIx93Uv2/TRxzG8ZfBxJTYJU5MCD9SsOIgogAtSAWCKCxkgSWtyhDUDmUofwAr/wAjEgMDUqUOCCG1Q6qqiAgqgoSCQOFHRUoRAkOA4CYxpNQxJpAwxCbGicFMSDw3fO/ue89b97l7dHxoBcrMzxW1Uq2grKQHnlcKiGmxXqu4xUKCAibkPHJBj0vSJssDltrkK63qRX2qWlXRqufShv3jpG733oRMAZrttFXCcjWCZcsdM+Cy33QbKp6eo9NxtzwzWUHL6HNQm7nTgM165SoyT7UJKSfsFpmyB/3gizfqndJLj931wKBn5lmgTr1GMVUC6u3SKOZXKYLazSsxP3XXDf363ZaUERLRoFFCs7hGS4R9aZGIY+4HpCwquotRd1zW47xbJmbsq85qG6yzygoNRh12NOC0bfmTzxrQq8tZw28NX7UWO2wVF3GITjf9b8ygU74Te3d489cf1eEnfwQEfK/DfH/6xZ2ZSXsHJvRe6z9SFTK9RkLWWAWOKmutcbswnJP/NtmvbZZIz9QG+2yfHhYAl2TssfH1uJzivtagZ2YJGf9p1yJlcJYIF5Sw1w4XHZcrBUxab5uE5UJGPJ3FHLbdXp9bIOu6f0sB6/zoodNCNmsVEzQuZxIBEQltvrVTULfrmjS4VjjwwgNWK+mMi+K+0W6Lv6SlZY0LC1uixhbn/KxXyBOf+aSwgwLghqQhGVdENavx2DItlqnXJ2tYn5X69RtFl1rpUsCj1yUlVDnid1Er7NHhgLSUcSGrNBnAiJHpoyl9g4Mm/O2CF4bkJI25mv9zUkfxU1peC9Xle9U6dRUlJiZcCUCRZaHW97N8CL0Ce/rLi5HPa/UAAAAldEVYdGRhdGU6Y3JlYXRlADIwMTktMDYtMTlUMjI6MzU6MTArMDI6MDCLScc3AAAAJXRFWHRkYXRlOm1vZGlmeQAyMDE5LTA2LTE5VDIyOjM1OjEwKzAyOjAw+hR/iwAAABl0RVh0U29mdHdhcmUAd3d3Lmlua3NjYXBlLm9yZ5vuPBoAAAAASUVORK5CYII="> <img src="https://img.shields.io/badge/-ear-lightgrey.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAQAAADZc7J/AAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAAmJLR0QAAKqNIzIAAAAJcEhZcwAADsQAAA7EAZUrDhsAAAAHdElNRQfjBhQAJgG45kVWAAACF0lEQVRIx53VS2yNURAH8N+tptEiVaIS0sQjlVgJC1KNRUNshHikS4mQxkIi7Gx0SWsh1IrEzhYJohILiSBeC68ECyuJij48mlZf19icXlfdtt/1/5Iv35yZ/5wzM9/MySmNxXbbZY0G4aM3rrlpSEbM025QTHl6tJmThb7S6yLakOEiqduC2eiNvhSMWy0C9Q54klZfqJuJXuutEHptn6LJaTMihNszBXJOCJ+tTnKlVVapTFKLn0I4Pn30o0Jec0plp34h9OtQAw4JoU9taQcnhXAFLPDsrxo8NR88EMLR0g6eC2EzuJSIrwo1uQh2CuFeKXqFMeGrCtQZE/L2gH3ywpiFmGtIGJH718FSIbwE21K+J9EthK3gjRCW/Nl3EnkTeAcWgg8F3UMwWvSumlRVFoz67LXF+VR1iKLyVvrkAWjAuB4zolUIXSU0jUJ4X5y68rAD3M3moFTj7Ac3ZtunNdX+zpR/rlkIn/6kcDqsky+4KMYtIZzMEmuzU2kSbCqsbRTCsPqsCTsthCNJynkkhM6/jWZK4jLwK0kHNeG7M1n2zjnhoRDyGsGiNKmOZTt8S6GNz6WVy6mpM41VVhgUBrWnEHcLYdz6rOmj3gbV6Xu5XiF0ZKcXo9pjIbwuOCwLFa4L4Ye1/0PPuSCEidREZdO7Ui2OlkOrclWfAQO+JXpnOXSaplyqZ8s9eI37RTfy4dnMfwMzau7RjZ7PmAAAACV0RVh0ZGF0ZTpjcmVhdGUAMjAxOS0wNi0xOVQyMjozODowMSswMjowMBRqR60AAAAldEVYdGRhdGU6bW9kaWZ5ADIwMTktMDYtMTlUMjI6Mzg6MDErMDI6MDBlN/8RAAAAGXRFWHRTb2Z0d2FyZQB3d3cuaW5rc2NhcGUub3Jnm+48GgAAAABJRU5ErkJggg=="> <img src="https://img.shields.io/badge/-forehead-lightgrey.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAQAAADZc7J/AAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAAmJLR0QAAKqNIzIAAAAJcEhZcwAADdcAAA3XAUIom3gAAAAHdElNRQfjBhQAJDNCB3ZUAAAEa0lEQVRIx3XVW3DU5RkG8N/u/jcnopzM5iSZcggwJIEhyeCEoxKMKI6jVFqlTpmqo1NtL9o602mv2l60t/WiWnvDoVMGaSkzHogmIqkuyqSBQiiVCGgawRw2EEsOsGST7UWWLQf73n3vfM/zfu/pe0Jut7CYNRotFVOCXgknHBQ3YPLWy6FbzoF6T1uhS9wJ/YYwS7FlVlmo3XYdUv+foNo2i3yoVa9r7rRWlRnGfabT5+50vzW67HDq6whCmmzRp9kZQ4p820ZdulxSqNwyCX9xRpmHFNurVfpmgpCt1jmpRbekxZ4yW7OzhiRFTVOsTr2/aVHoATXa7J6iiGQIHrBRh7d0S6mwyRw7faTXiCtGDbngvEkr5TnmnGlWuurc/wiqbdPpbRekRa2zyj5x4zfVZ9h50yxHhz6zrHdOYoog8BOX7dcjjfnuNWaPa7e196o+C1To8YWvLFDrkMkw6s31jh6TiKpXpMWYr7N+h0WsNOFzByxWRyDsaXGfSoI5Kl10/AbQXaoVCAn0GjQiR41cSZ+K+572QEytV32VGaMGBZqz8UMKbTVPxCIzdTrtqrkuu0PSJS22iwXWOOWCcUwzR40hR7PRczTZ4rd6bFZkzHSBtJBCg1L6nLE60Oi0XDPNUmWdSXEjGXjUIj/ya63G/T2zJaUC883WjTFxjYEaoxqF3Wehu7ySjR9R7ofaHci+J6LUNt9x0hWQ1OlbgWIF1opq8UsvusMMfYgos8U8j2TBUSV+bLHTejK+CQOKA0V+bijjesujmuwSqPGSmOeMZmqx1FrfdLd3paV8liG4KBbc1Oc2y9XrVm2rN7wsiUc9p9Z57d5V6R4feM3VG0Fn3S2cPVV5WZfXrZWHHI876gkVpitwjwPetyl7O7DEmUC/CgOZwZ1tg0p77fSFpDzr/MwL/mXUpNVWyNPqw+yvFBHTF+hU5aRrQho8JeIPPjZoQp4Gv9HjlFGb3W+hXF86bjj72lxLdUbka9QmzzM2OeuvOlySlmu5lxxVqFynx6zQLOWswwazBDM9781A3E89rNa4FkcyMxmo9n3DXlXuV+ZYb499fmBAbxYeVapSPGzAMZsN2q9Zt3GELfGkmOnyHLZDoUCbAfnGslPKTE2OSIRN2q7Yccf8J7NACz2myHsqvajEXhe06THbhGET2fwXWWWHdBgdDqlTmmnPAlutNyJfh6gX5Kpx0JByYy5n6z/Xgz5xlDBSdiqyQamw+R7RINc8FX7n96o86xtOGlWSTSCkTJOYXVLX/8SEa+5ToFCTuf4tR6HXfCCh3y/8w34j7hX2TwlhZR5U68+OTE3TlLUqstLjRuxxyQwfew8pB33iTaOIuWhYjgobLHNI6/VxnLK03RKe0adPqcvarwuHY9pcQUyvfHU2KrHvdmG5vgnfNc+4lN0+kpQyKS0ikGOXE0atcM4fb5S2yE0ECW26ValTYYZAVFi+Yks02qDBRa/4k/4bIbeq85QvZnVG3svwpYGMvCeyiWXtv/mJfPVYOvIyAAAAJXRFWHRkYXRlOmNyZWF0ZQAyMDE5LTA2LTE5VDIyOjM2OjUxKzAyOjAwQkN5egAAACV0RVh0ZGF0ZTptb2RpZnkAMjAxOS0wNi0xOVQyMjozNjo1MSswMjowMDMewcYAAAAZdEVYdFNvZnR3YXJlAHd3dy5pbmtzY2FwZS5vcmeb7jwaAAAAAElFTkSuQmCC"> <img src="https://img.shields.io/badge/-hair-lightgrey.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAQAAADZc7J/AAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAAmJLR0QAAKqNIzIAAAAJcEhZcwAADdcAAA3XAUIom3gAAAAHdElNRQfjBhQAJyGak1TfAAACYElEQVRIx5XTTWhcZRTG8d/kg6QxTVMikgQ1E5BSbG1RcCNKxLpVwW1pNu4Et2oXreBWSjZdpKBu3IgfaFEx2JKNhWCUtKKWNjGokAmd2iSTzCSZZD6um5vpveOdZua8q3vPef7vOe85h/9bp5M+8JtNBde9b1S7FmzEOX/ZVlZVVbYt422PNCs/6ZIVZUHkVKz60tPN5JE2YSUm3jt5U8Z0Plie8qbbifJAoOCyF7TVizpi9z8n3QC+rseL7im4HndE63rea0YS5XdMGPaYIQUL8lFXNKW0gQRxxTUXfCwjMOhVY7GsY4A+3QmAjAkfyvpFFk96yeONAGXVOnFgyzemrQt85gerujzlmUaAu/HqUPG7j1TAr77yJ0Ydi6qigFvu1AGqFmQUBCCviAFpvcmAmxYVYyVlDDte69RRg2gz4NFkwIYZ8+FtVC15x1umlcPIohLoN3xfFGuJb53whB6Q87XPYz066mFwMLpa8dFc8anvBQgsm4z58obCOenW1ygDfnZe1rg1n7iNlJf1WrMp7UgYfcAhD7B2/Z71ikPocVFe3oYNBaVwrf5xtnEGVKy7oUNRpyPGoy0LLQgnI+EN9gJKtgUqcjYT/NWwLw0B9wOz3lWsNXbPtuSaA1B02UU7dX/z/m0WEMiZNFOHyFluFgCLJq1FyihZ9ncrAKb8EcnhrnmrrQE2/KRQ+5o3F33WZgAs263VP+tG1NUc4HA4cLtmXI32YD9LOYxuXygIlMw57UDzcrq8YdApS6p23XTGQ63I6XXFd5bs2DLr9YS92MfanfCjVXPeMyKVFPIfTP7d9k/l0HAAAAAldEVYdGRhdGU6Y3JlYXRlADIwMTktMDYtMTlUMjI6Mzk6MzMrMDI6MDDiuDpZAAAAJXRFWHRkYXRlOm1vZGlmeQAyMDE5LTA2LTE5VDIyOjM5OjMzKzAyOjAwk+WC5QAAABl0RVh0U29mdHdhcmUAd3d3Lmlua3NjYXBlLm9yZ5vuPBoAAAAASUVORK5CYII="> <img src="https://img.shields.io/badge/-beard-lightgrey.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAQAAADZc7J/AAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAAmJLR0QAAKqNIzIAAAAJcEhZcwAADdcAAA3XAUIom3gAAAAHdElNRQfjBhQAKQBIeWkPAAACmUlEQVRIx8XTzWucVRQG8N+8M+lMJmnakFilYBHawSzSLESoQildiG0tpYgLcdmViIuCpeKu9B9wVVBEEaQgbvwgUFIXKtYKaqRqtWoxiY1N0ubD0mSm6WQ+rou8ma9ESLLQ56zuPec895x7zsP/j0H92jaV2abfIAXPy26KIOsFhUjWgPSmCNIGtEc4qH2TFRyEYN5TMhtOb3fIgmqErZ7RvWGCbkd1kgJHfWjOUkuHD+mVxT2zbik2ebfY4wgrBDmHjJmoubfZa6+cnTqRN+m6q352txaxw2G7EQiC4JrDtX/Y5rghhdizbHkXHNMVR2Qc8bsgqKiFnPOoBCIHXGhKXrFB+0VI6PNGfNdAcNtLeiR0e819QVBVMG7cPVVBsOhV2yX0eNlMnFVOOiMBOjxsxl/6PGdAUDTpG+d8JistI6nNHX9YdMxJj8TNVCjE/EEw6ozTfhLkDdkXUyc8YUhe8IPTzvqzFl81y02Vhj6rSkqC7+1rGtt+VwQlpYbngrJfItdVGwITUlLKJg03EXxrSkVKKq5qGcFUypeejLehjiXzUvo8Hp+/M2Le0irNlA2nDHllDSUEXZ51Mj697m1hjXUuuRj50Q3lFkfaDnyOXr2qvpDwwCrRV9w2HFl03kKLKynnhLRRMCLjhD2ilqi89+Vhl68VW7buvhGXTAuCWy4ZjZerbiVX5FZ+/kU3msazHptwSkQSTOixW4f1Y9ZH3mxQp37vmVv363d84LGV71rGtFkZD+psWpS1EMy46B2XmwkYNybSo3PVWjWiaMwn3vJVfWB1TLvmb2kZmTVJlkwZdt67fq1fthackHPc03bp0mGLZCyhRQtu+tTHLdr5l4636ndAv522K5oz4zeXXTW/gTn9Z/gHWiE0zL9ql14AAAAldEVYdGRhdGU6Y3JlYXRlADIwMTktMDYtMTlUMjI6NDE6MDArMDI6MDBnM3JQAAAAJXRFWHRkYXRlOm1vZGlmeQAyMDE5LTA2LTE5VDIyOjQxOjAwKzAyOjAwFm7K7AAAABl0RVh0U29mdHdhcmUAd3d3Lmlua3NjYXBlLm9yZ5vuPBoAAAAASUVORK5CYII="> <img src="https://img.shields.io/badge/-face-lightgrey.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAQAAADZc7J/AAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAAmJLR0QAAKqNIzIAAAAJcEhZcwAADdcAAA3XAUIom3gAAAAHdElNRQfjBhQAKzUs/M+uAAADy0lEQVRIx53VbWgVVBwG8N/uXdts2506ndPpXEyXGRtLS/CVfEsig3CgCAqRrDeFIqoPfREKEgIJhF4EzRIniCVlJRJEljrfpja1dG65abqp29yuerd53Xb7srndLUn6f/tzznl4zv95znMSDKxCJdqt1+l/1SQbRVR7+0EPBOO6kFVWuKtLnosuPChAphxZkkTNtkLEp6oslOp7ibJlSnRX7H4AiQpskCFBp6tGGW+HHR41x3yfy5EuoFPUDWcdVqFxMIOhPjBcPQpM0GS3AxLkWGi8ZGEjFEs3TpFpJutyzZ14Bg1apPrSJQVekiAspk2TiH3KtFojX5k/jDbdXAVyfaehP0Cbo57R7qhTZiuUjERD3LbPt5Kt0+4bx6T71QKLlQrarqUXIICv3VFionYtQkYJyPCIDrUe8qxCR9SKarbfRlt0W2mBQH8VrpliuoBGoxTpUG2i5SK2m+pdIR865S64pU6ymUao6OUQRLsW+eYaI0WO8UYqNkO9iNUm2GazyL0rR9wy1hMaHY9XY6FtqjW4LSYmpkOD6yqtlyEhbmeyVeqUSYp34gXlmg2VhauuuqXZQRt8omOA8F2GmmK4n4QH26rQTse84klz5Q9aTejhUmSrk2b1ythf0jQpWp13XEAMAQm6xRA0RJpOt0W1C0sxWpKoPjkw06ue0qVLyGT5grIV98zgcWVqVHpLlm6dxnlNSfx0ljstJmavOZ5W6bJ1TospFhS0121nXHbFG/J9LCamxdo+BomWybTTIfCnr2R4U76tTuuSa4wj1njZJhcEUeszzUqFemcwzDB19kkTcF2zrU6Y7IpyXXhYoptaHVYuKlW5m07JtMjYXoCwVlNl2eO6Rl2aHVIpKoIir8v2i4gOHej0myqFpoio75vBSiddUO4jRQPkW6bG756X2tOPsdp+Z1zzvkBfpDVokK5IouPq4gC6nbfLEbd6+mzPWaTaZtu19vmg0Y+aZEiXNoBBjVpR3ff6IUIabPWDpngf3HRCrUw5/Xy/2ntypUnpt3O4XDcc0DTQiYRdlGySkJs94k5VIk/Yzw71eD9ZnlzHe1MpPta7hRTKVq0WxLTK9ZhJLjrX86gLLJVnl/3/BkCb0WYY4rQwutU56y/HHHPFXYywxAuqbHLdfWquPaqslTsgB0gw0ov2q1TatxYcBHBVxDSzhFzRKdrzpQSkG6dEqSxltvSlxGCATpfUKzbPfLRJkm6oHPO8Y6luX9jkhv+oREU2a9KmXY0K54S1abXHYikD73W/SlJgiQXyZQr720G7VQyOsX8AWVVMln82rkkAAAAldEVYdGRhdGU6Y3JlYXRlADIwMTktMDYtMTlUMjI6NDM6NTMrMDI6MDAazraUAAAAJXRFWHRkYXRlOm1vZGlmeQAyMDE5LTA2LTE5VDIyOjQzOjUzKzAyOjAwa5MOKAAAABl0RVh0U29mdHdhcmUAd3d3Lmlua3NjYXBlLm9yZ5vuPBoAAAAASUVORK5CYII="> <img src="https://img.shields.io/badge/-head-lightgrey.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAQAAADZc7J/AAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAAmJLR0QAAKqNIzIAAAAJcEhZcwAADsQAAA7EAZUrDhsAAAAHdElNRQfjBhQALSAXe4zDAAABpUlEQVRIx52TzStEURiHHx8zI0bTTBaIFE26U1KGhY9BWZCykIVkY6FkYUHZWqgpWdlYK1n4C5SFrIQNSVLKRr7SFFFSuNdi3Dv3zNx7z7nzO5vz0e8573nf85bgpDZS9KIRJUYlGTLcsM8e90hVyhjHGI7jl23qvO0Jzl3M5nhj2N3ew6vEbmDwRb+zvZFnBbuBwR2RnK3Mmu2hyVMEQIQfDvM3RxRvz44MgXzAgS+AwVCubABhUorhm+oWAanCkCRqFAEJn3YIi4Cob0BABMRsR1+s0EkL456AR3NSDsCn7WiOXaaoJe4JeBGXy7aGCbGmUMYt8QknFqoE0BVyME3SvgzyYrEH6VX6StdUgdkLv1QyaME26KBVGkMN7xzlllXc/pN1RgkyyQwN7HjGMC8Sk3xYHZ8mRQcLng2+XhjUAG8+2qnP6V1xzhTtl26pCbGpBFhyz24YXWrXaXIHLCrcf+pVX3kW3p0TaKqdCwfTBRNoxGhGo1r2x4Ks8i3Yn4SGV1KSSxtg1q89W9C0FUd9MQCALq4wMKgoFgAh1njINq6z/gB3dX6e/ABoKQAAACV0RVh0ZGF0ZTpjcmVhdGUAMjAxOS0wNi0xOVQyMjo0NTozMiswMjowMHfIxOAAAAAldEVYdGRhdGU6bW9kaWZ5ADIwMTktMDYtMTlUMjI6NDU6MzIrMDI6MDAGlXxcAAAAGXRFWHRTb2Z0d2FyZQB3d3cuaW5rc2NhcGUub3Jnm+48GgAAAABJRU5ErkJggg=="> <img src="https://img.shields.io/badge/-man-lightgrey.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAQAAADZc7J/AAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAAmJLR0QAAKqNIzIAAAAJcEhZcwAADsQAAA7EAZUrDhsAAAAHdElNRQfjBhQALyO8RL/7AAABm0lEQVRIx53UPU8UURTG8d+uu2B8IZCl0GAkGpQoCdaGjspGEwuNIe4HMNYamq1MtNKPgAUmFBiyn4AOTVb9ABZgBLYQCwvXKAEyFgjZ2XnZO55bTCbnPP879zn3DFlx2lMtHR0tT5xSMKZsiLrWuqki8vPaMXkk0nYuHPA6IY9EFkLlZ/xOBfxxNllcTgHccDIVPGg6DDCU+W1DYYDtTMBWmAclW6kebCqF2vg4FfAoVE7Z24R8OXx/qHhht6uBz1WyzpsdY+66is+a2kV2LxT55xoxi1U/QnEDbpm36KMGeCUSeQkaPlk0bzZbPuPLsW3fDeCSn36ZQNXOce69K2ny6zqxtt0BTU1wO5bbNp4ErCT6Dh+0wHJP9k2vvOYgMbwj2PENw4kB3zd8KDwapsnEWA26p6pmVNX9xICfcC0OqKW4UrfnnTV76inZ0cNHxgX915XLFjBuJrsoD1Dy0DM08q5bWV7UEZnLK6nkAibcFJn8fwBLffJ9ARf7Acr9CkIBB4WV+/HXC10/sJC1a6yXOGczWP7VgyPZX/XY5WnC1EU7AAAAJXRFWHRkYXRlOmNyZWF0ZQAyMDE5LTA2LTE5VDIyOjQ3OjM1KzAyOjAwtpoqUwAAACV0RVh0ZGF0ZTptb2RpZnkAMjAxOS0wNi0xOVQyMjo0NzozNSswMjowMMfHku8AAAAZdEVYdFNvZnR3YXJlAHd3dy5pbmtzY2FwZS5vcmeb7jwaAAAAAElFTkSuQmCC"> <img src="https://img.shields.io/badge/-woman-lightgrey.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAQAAADZc7J/AAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAAAmJLR0QAAKqNIzIAAAAJcEhZcwAADdcAAA3XAUIom3gAAAAHdElNRQfjBhQAMC4Pr83YAAAB30lEQVRIx53VzUtUYRTH8c84+TIzluPbCOVooIW0sKIQahERREVLoQhrEwT9Ef0r0apN61YF5cpeyI0EWWiEhkVFqeWImk6LIZy5c1/U39k9z/19n3POfe65hCuly13jlq2adk+PXSnrspdWbNiy5a+SVx64qm1n9pxr3llTrop1f3x0x/5ke8olL2zU2Cux6bFzwccb6gADrjhhXwi6wYhjQUc9YNh5LRHZdeiXjwfkDDkSWV5ap/Z4QEGfbGyDc/GADh2xLc7IJJWQiwW0BPsTBNSdEFCz5nhAk6ZYQN3+bjNILKE9+JqS9msBKd26YgHdClLRgG7FhM/lgKLOaMApQ5I05HQUIOOC44mAky5WNzpdtXXDmP7aCkPUJGPJVFgGBW2JdlLyCuEZLHhrXllrxF0o+2nSI/c9s7TNq1ZWwUE9RowpBuzzHnrtqy++KW0v106ekjm/bVrTWHd+ozULZvyyVVvRf+UNGnBYUa9BR+sQGz6Y8dm8T2bNWKwGZJ11xrABffI1fQlq06I5s6ZMmLBaWWx1y1PLIXM4OpY9cVNrJYdR70PHeHxsmDYqRa9J67u2V342bxxKu+165BiPV1reAuN7SH+7jOcp33Xu4AKHq+xHgxXlPdopK/0DLXHVg2ZxessAAAAldEVYdGRhdGU6Y3JlYXRlADIwMTktMDYtMTlUMjI6NDg6NDYrMDI6MDB8vGJaAAAAJXRFWHRkYXRlOm1vZGlmeQAyMDE5LTA2LTE5VDIyOjQ4OjQ2KzAyOjAwDeHa5gAAABl0RVh0U29mdHdhcmUAd3d3Lmlua3NjYXBlLm9yZ5vuPBoAAAAASUVORK5CYII=">

## What is PARTNet
PARTNet is a compact model trained to be faster and smaller.
The initial idea of this project is train a model to detect human head parts and expand to the entire human body.
Our model is trained over [ONNX](http://onnx.ai), this allows the model to be executed in real time on mobile devices and embedded devices, it also allows the model to be converted to other neural network architectures.
The model is not as accurate as a full model, but it's being constantly updated for best results.

## What is ONNX?
The Open Neural Network eXchange ([ONNX](http://onnx.ai)) is an open format to represent deep learning models. With ONNX, developers can move models between state-of-the-art tools and choose the combination that is best for them. ONNX is developed and supported by a community of partners.

## Model Visualization
You can see visualizations of each model's network architecture by using [Netron](https://lutzroeder.github.io/Netron) or [VisualDL](http://visualdl.paddlepaddle.org/).

### Run samples
We offer the model in 3 different formats: ONNX, CoreML and TensorFlow. Download according to the last registered timestamp, the format is: **dd_mm_yyyy__hh_mm_ss**. To execute them simply unzip the specific file and run the command:

```bash
python python/onnxruntime_predict.py <image_file>
```
or

```bash
python python/predict.py <image_file>
```

[![Visualizer badge](https://img.shields.io/badge/visualizer-netron-blue.svg)](https://lutzroeder.github.io/Netron)
[![Visualizer badge](https://img.shields.io/badge/visualizer-visualdl-blue.svg)](http://visualdl.paddlepaddle.org/)

## Statistics
[![Legend badge](https://img.shields.io/badge/-precision-blue.svg)]()
[![Legend badge](https://img.shields.io/badge/-recall-orange.svg)]()
[![Legend badge](https://img.shields.io/badge/-mAP-green.svg)]()

<p align="center">
<img src="/statistics/precision.png" width="30%"/>
<img src="/statistics/recall.png" width="30%"/>
<img src="/statistics/mAP.png" width="30%"/>
</p>

These are the statistics of the last iteration performed. They are based on a subsample of the original image database that contains 60,000 images.

### Performance Per Tag

| Probability Threshold | Overlap Threshold |
| --- | --------- |
| 50% | 30% |

| Tag | Precision | Recall | A.P. | Image Count |
| --- | --------- | ------ | ---- | ----------- |
| Human beard | 78.6% | 10.8% | 34.9% | 5044 |
| Man | 38.3% | 1.8% | 13.3% | 5087 |
| Human hair | 33.3% | 0.0% | 6.5% | 5105 |
| Woman | 30.4% | 0.2% | 10.7% | 5059 |
| Human head | 20.0% | 0.0% | 5.9% | 5123 |
| Human ear | 11.8% | 0.1% | 4.8% | 5071 |
| Human eye | 11.1% | 0.0% | 5.5% | 5115 |
| Human nose | 0.0% | 0.0% | 3.1% | 5121 |
| Human face | 0.0% | 0.0% | 6.9% | 5090 |
| Human eyebrow | 0.0% | 0.0% | 5.0% | 5081 |
| Human forehead | 0.0% | 0.0% | 5.3% | 5094 |
| Human mouth | 0.0% | 0.0% | 3.8% | 5116 |

## Dataset
We use a subset of images extracted from Google Open Images Dataset V5 ([OIDV5](https://storage.googleapis.com/openimages/web/factsfigures.html)) containing 60,000 images that were randomly extracted using the [OIDv4_ToolKit tool](https://github.com/EscVM/OIDv4_ToolKit). 
The database is really great, if you have interest contact us by [email](mailto:claudemir.casa@ufpr.br).

## Contributions
Do you want to contribute a model? To get started, pick any model presented above with the [contribute]() link under the Description column. The links point to a page containing guidelines for making a contribution.

## License
[![License badge](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

MIT License. Copyright (c) 2019 IMAGO Research Group.

## Authors
[Claudemir Casa](claudemir.casa)

## Collaborators
Special thanks to my lab colleagues.

[Jhonatan Souza](https://github.com/xkiddie)
[Tiago Mota de Oliveira](https://github.com/tiufsc)
