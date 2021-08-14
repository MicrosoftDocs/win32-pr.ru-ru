---
title: асфлеакибуккетпаирс
description: Атрибут Асфлеакибуккетпаирс является необязательным атрибутом, который описывает требования к буферизации для файла переменной скорости.
ms.assetid: d1b3e8cc-c082-4283-88bc-172f58adf2d9
keywords:
- Формат Windows Media Асфлеакибуккетпаирс
topic_type:
- apiref
api_name:
- ASFLeakyBucketPairs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76de649a069b0cfec74fabe1a41d6cfa659b39448257a4bc966065e1bce98ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434623"
---
# <a name="asfleakybucketpairs"></a>асфлеакибуккетпаирс

Атрибут **асфлеакибуккетпаирс** является необязательным атрибутом, который описывает требования к буферизации для файла переменной скорости.

## <a name="global-constant"></a>Глобальная константа

g \_ всзасфлеакибуккетпаирс

## <a name="data-type"></a>Тип данных

**\_ \_ двоичный тип ВМТ**

## <a name="remarks"></a>Remarks

Этот атрибут имеет следующий формат:

``` syntax
struct
{
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

Где *вресервед* должно равняться нулю, а *контейнер* — массив [**\_ \_ \_ пар сегментов с утечкой**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) данных типа WM. Массив должен содержать по крайней мере две записи, но может быть больше. Объект "читатель" использует этот атрибут для определения объема содержимого для буферизации перед воспроизведением.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




