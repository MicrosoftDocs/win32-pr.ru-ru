---
title: Структура Вмдмметадатавиев
description: Структура Вмдмметадатавиев определяет представление метаданных. Содержимое организовано на основе этого определения.
ms.assetid: 787d2295-d433-451d-a1fc-6f73585e10d6
keywords:
- Структура Вмдмметадатавиев Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMDMMetadataView
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aa38a8fe7f19137c5caff18417d48ea23168b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694463"
---
# <a name="wmdmmetadataview-structure"></a>Структура Вмдмметадатавиев

Структура **вмдмметадатавиев** определяет представление метаданных. Содержимое организовано на основе этого определения.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WMDMMetadataView {
  WCHAR *pwszViewName;
  UINT  nDepth;
  WCHAR **ppwszTags;
} WMDMMetadataView;
```



## <a name="members"></a>Члены

<dl> <dt>

**пвсзвиевнаме**
</dt> <dd>

Указатель на строку расширенных символов, заканчивающуюся нулем, которая содержит имя представления. Используется в качестве имени корневого узла, в котором представлено это представление.

</dd> <dt>

**ндепс**
</dt> <dd>

Целое число, содержащее глубину представления, которое указывает, сколько тегов вложенных метаданных используется для представления.

</dd> <dt>

**ппвсзтагс**
</dt> <dd>

Массив строк тегов метаданных для вложенных тегов.

</dd> </dl>

## <a name="examples"></a>Примеры

Следующий код создает представление метаданных:


```C++
WMDMMetadataView view;
view.pwszName = L"My View";
view.nDepth = 3;  // genre, artist, album
LPCWSTR wszTagArray[3]; 
wszTagArray[0] = g_wszWMDMGenre;
wszTagArray[1] = g_wszWMDMAuthor;
wszTagArray[2] = g_wszWMDMAlbumTitle;
view.ppwszTags = wszTagArray;
```



Приведенный выше код организует содержимое следующим образом:

<dl> Мое представление<dl> Genre1<dl> Artist1<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> </dl> </dd> Genre2<dl> Artist1<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> ...  
</dl> </dd> ...  
</dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры**](structures.md)
</dt> </dl>

 

 





