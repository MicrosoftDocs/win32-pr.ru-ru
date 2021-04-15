---
title: Структура МЕНУХЕЛПИД
description: 'Содержит окончательные данные, записанные в \_ ресурс меню RT для меню или подменю, если элемент Resinfo: структуры попупменуитем имеет значение МФР \_ Popup.'
ms.assetid: f17fdaaa-b37c-4902-bad4-a1181ffee9f9
keywords:
- Меню структуры МЕНУХЕЛПИД и другие ресурсы
topic_type:
- apiref
api_name:
- MENUHELPID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b90b5a4745433c92a859a168611aa1c14f1fa45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661979"
---
# <a name="menuhelpid-structure"></a>Структура МЕНУХЕЛПИД

Содержит окончательные данные, записанные в ресурс [**\_ меню RT**](/windows/desktop/menurc/resource-types) для меню или подменю, если элемент **Resinfo:** структуры [**попупменуитем**](popupmenuitem.md) имеет значение **МФР \_ Popup**. Приведенное здесь определение структуры предназначено только для объяснения. он отсутствует в любом стандартном файле заголовка.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD helpID;
} MENUHELPID;
```



## <a name="members"></a>Члены

<dl> <dt>

**Идентификатор справки**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Идентификатор, используемый для идентификации меню во время [**обработки \_ справки WM**](/windows/desktop/shell/wm-help) .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**менухеадер**](menuheader.md)
</dt> <dt>

[**попупменуитем**](popupmenuitem.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Ресурсы](resources.md)
</dt> </dl>

 

