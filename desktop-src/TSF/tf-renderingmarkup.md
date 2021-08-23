---
title: Структура TF_RENDERINGMARKUP
description: '\_Структура структуры TF рендерингмаркуп содержит диапазон и сведения об атрибуте вывода.'
ms.assetid: 206e679b-f2eb-4f28-ac2a-58f3c222a020
keywords:
- Инфраструктура текстовых служб TF_RENDERINGMARKUP Structure
topic_type:
- apiref
api_name:
- TF_RENDERINGMARKUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d594ae41109e072413e20709c68770038fbae870966325f762ddd169900491d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118874207"
---
# <a name="tf_renderingmarkup-structure"></a>\_Структура TF рендерингмаркуп

Структура структуры [**tf \_ рендерингмаркуп**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) содержит диапазон и сведения об атрибуте вывода.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  ITfRange*           pRange;
  TF_DISPLAYATTRIBUTE tfDisplayAttr;
} TF_RENDERINGMARKUP;
```



## <a name="members"></a>Члены

<dl> <dt>

**пранже**
</dt> <dd>

Указатель на интерфейс [итфранже](/windows/desktop/api/Msctf/nn-msctf-itfrange) .

</dd> <dt>

**тфдисплайаттр**
</dt> <dd>

Отображение сведений об атрибутах.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта структура в настоящий момент не находится в файлах общедоступного заголовка. Чтобы использовать этот API, необходимо скомпилировать [прототип](prototypes.md)с помощью MIDL.

 

 




