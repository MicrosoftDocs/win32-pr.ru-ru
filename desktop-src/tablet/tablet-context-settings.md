---
description: Содержит сведения, используемые при создании контекста планшета.
ms.assetid: 10466c23-f4cb-4205-886b-d85a2f530afe
title: Структура TABLET_CONTEXT_SETTINGS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_CONTEXT_SETTINGS
api_type:
- NA
api_location: ''
ms.openlocfilehash: 75634cd635773ff0b009860256b1147c31ee43dde200586e12713a707aa999b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119335084"
---
# <a name="tablet_context_settings-structure"></a>\_Структура параметров контекста планшета \_

Содержит сведения, используемые при создании контекста планшета.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _TABLET_CONTEXT_SETTINGS {
  ULONG cPktProps;
  GUID  *pguidPktProps;
  ULONG cPktBtns;
  GUID  *pguidPktBtns;
  DWORD *pdwBtnDnMask;
  DWORD *pdwBtnUpMask;
  LONG  lXMargin;
  LONG  lYMargin;
} TABLET_CONTEXT_SETTINGS;
```



## <a name="members"></a>Члены

<dl> <dt>

**кпктпропс**
</dt> <dd>

Число свойств в пакете.

</dd> <dt>

**пгуидпктпропс**
</dt> <dd>

Уникальные идентификаторы для свойств пакета.

</dd> <dt>

**кпктбтнс**
</dt> <dd>

Число кнопок.

</dd> <dt>

**пгуидпктбтнс**
</dt> <dd>

Уникальные идентификаторы для кнопок.

</dd> <dt>

**пдвбтнднмаск**
</dt> <dd>

Маска кнопки "вниз".

</dd> <dt>

**пдвбтнупмаск**
</dt> <dd>

Кнопка "вверх".

</dd> <dt>

**лксмаргин**
</dt> <dd>

Поле направления по оси X.

</dd> <dt>

**лимаргин**
</dt> <dd>

Поле направления по оси Y.

</dd> </dl>

## <a name="remarks"></a>Remarks

Как правило, приложение получает значения по умолчанию из [**метода итаблет:: жетдефаултконтекстсеттингс**](itablet-getdefaultcontextsettings.md), изменяет значения в соответствии с их потребностями, а затем передает измененную структуру параметров в [**метод Итаблет:: CreateContext**](itablet-createcontext.md).

эта структура определяет, какие события будут получены приложением, как они будут обработаны и как они будут переданы в приложение или Windows себя.

На кнопке маски группируются, чтобы определить, какие типы событий будут обрабатываться контекстом.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                     |



 

 




