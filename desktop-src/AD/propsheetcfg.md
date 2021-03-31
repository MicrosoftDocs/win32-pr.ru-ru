---
title: Структура ПРОПШИТКФГ
description: Используется для хранения данных конфигурации страницы свойств.
ms.assetid: d3bde744-9d85-4506-894f-f8be3463721f
ms.tgt_platform: multiple
keywords:
- Active Directory структуры ПРОПШИТКФГ
- Active Directory указателя структуры ППРОПШИТКФГ
topic_type:
- apiref
api_name:
- PROPSHEETCFG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33f4a1186cc756435cc49ed7c81592385faaee60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071660"
---
# <a name="propsheetcfg-structure"></a>Структура ПРОПШИТКФГ

Структура **пропшиткфг** используется для хранения данных конфигурации страницы свойств. Эта структура содержится в формате буфера [**обмена \_ \_ пропшитконфиг DS кфстр**](cfstr-ds-propsheetconfig.md) .

> [!Note]  
> Эта структура не определена в файле опубликованного заголовка. Чтобы использовать эту структуру, необходимо определить ее самостоятельно в указанном формате.

 

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  LONG_PTR lNotifyHandle;
  HWND     hwndParentSheet;
  HWND     hwndHidden;
  WPARAM   wParamSheetClose;
} PROPSHEETCFG, *PPROPSHEETCFG;
```



## <a name="members"></a>Члены

<dl> <dt>

**лнотифихандле**
</dt> <dd>

Содержит маркер уведомления. Это идентично маркеру, переданному для параметра *Handle* в методе [**IExtendPropertySheet2:: креатепропертипажес**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) .

</dd> <dt>

**хвндпарентшит**
</dt> <dd>

Содержит маркер окна родительской страницы свойств.

</dd> <dt>

**хвндхидден**
</dt> <dd>

Содержит маркер скрытого окна.

</dd> <dt>

**впарамшитклосе**
</dt> <dd>

Содержит определяемое приложением 32-разрядное значение. Это значение передается обратно в приложение в параметре *wParam* сообщения [**\_ \_ \_ \_ о закрытии страницы WM DSA**](wm-dsa-sheet-close-notify.md) .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ПРОПШИТКОНФИГ кфстр DS \_**](cfstr-ds-propsheetconfig.md)
</dt> <dt>

[**\_ \_ \_ уведомление о закрытии листа WM DSA \_**](wm-dsa-sheet-close-notify.md)
</dt> </dl>

 

