---
title: Структура МЕНУХЕАДЕР
description: Содержит сведения о версии для ресурса меню. Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.
ms.assetid: 1e34b0b6-18ff-4cb6-901e-a2aabad0df74
keywords:
- Меню структуры МЕНУХЕАДЕР и другие ресурсы
topic_type:
- apiref
api_name:
- MENUHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e78b577d52f0e40737f90186903aff9bfe2470d7050eac1ee00bc79ca7f596f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972013"
---
# <a name="menuheader-structure"></a>Структура МЕНУХЕАДЕР

Содержит сведения о версии для ресурса меню. Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  WORD wVersion;
  WORD cbHeaderSize;
} MENUHEADER;
```



## <a name="members"></a>Члены

<dl> <dt>

**вверсион**
</dt> <dd>

Тип: **слово**

</dd> <dd>

Номер версии шаблона меню. Этот элемент должен быть равен нулю, чтобы указать, что это [**\_ меню RT**](/windows/desktop/menurc/resource-types) , созданное с помощью стандартного шаблона меню.

</dd> <dt>

**кбхеадерсизе**
</dt> <dd>

Тип: **слово**

</dd> <dd>

Размер заголовка шаблона меню. Это значение равно нулю для меню, создаваемых с помощью стандартного шаблона меню.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**\_заголовок шаблона \_ менуекс**](menuex-template-header.md)
</dt> <dt>

[**\_элемент шаблона \_ менуекс**](menuex-template-item.md)
</dt> <dt>

[**менуитемтемплате**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)
</dt> <dt>

[**менуитемтемплатехеадер**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)
</dt> <dt>

[**нормалменуитем**](normalmenuitem.md)
</dt> <dt>

[**попупменуитем**](popupmenuitem.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Ресурсы](resources.md)
</dt> </dl>

 

