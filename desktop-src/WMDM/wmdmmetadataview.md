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
ms.openlocfilehash: 8e442ed3058f1982ac7607c6b8a29e5df321d69776695821b278049e27cd7589
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862594"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Структуры**](structures.md)
</dt> </dl>

 

 





