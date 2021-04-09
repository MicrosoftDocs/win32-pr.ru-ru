---
title: Структура DSA_SEC_PAGE_INFO
description: Используется с \_ листом WM адспроп на листе \_ \_ CREATE и WM \_ DSA \_ \_ Создание \_ уведомления об уведомлении для определения дополнительной страницы свойств в оснастке консоли MMC Active Directory.
ms.assetid: 422d84dc-6b5e-43bf-ac4f-3b99cb59f9df
ms.tgt_platform: multiple
keywords:
- DSA_SEC_PAGE_INFO структуры Active Directory
- PDSA_SEC_PAGE_INFO Active Directory указателя на структуру
topic_type:
- apiref
api_name:
- DSA_SEC_PAGE_INFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e4c8602a958c50c72942d89657a812d24f64571d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988919"
---
# <a name="dsa_sec_page_info-structure"></a>\_ \_ \_ Структура сведений о странице DSA sec

Структура **\_ \_ \_ сведений о странице DSA sec** используется с листом [**WM \_ адспроп \_ листов \_ CREATE**](wm-adsprop-sheet-create.md) и [**WM \_ DSA \_ \_ Создание сообщения \_ уведомления**](wm-dsa-sheet-create-notify.md) для определения дополнительной страницы свойств в оснастке консоли управления Active Directory MMC.

> [!Note]  
> Эта структура не определена в файле опубликованного заголовка. Чтобы использовать эту структуру, определите ее в точно указанном формате.

 

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _DSA_SEC_PAGE_INFO {
  HWND          hwndParentSheet;
  DWORD         offsetTitle;
  DSOBJECTNAMES dsObjectNames;
} DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**хвндпарентшит**
</dt> <dd>

Содержит маркер окна родителя страницы вторичного свойства.

</dd> <dt>

**оффсеттитле**
</dt> <dd>

Содержит смещение в байтах от начала структуры **\_ \_ \_ сведений о странице DSA sec** до завершающейся нулем строки Юникода, которая содержит заголовок дополнительной страницы свойств.

</dd> <dt>

**дсобжектнамес**
</dt> <dd>

Содержит структуру [**дсобжектнамес**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) , определяющую вторичную страницу свойств. За раз можно создать только одну вторичную страницу свойств, поэтому структура **дсобжектнамес** может содержать только одну структуру [**дсобжект**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ Создание листа WM \_ адспроп**](wm-adsprop-sheet-create.md)
</dt> <dt>

[**\_ \_ \_ уведомление о создании листа WM DSA \_**](wm-dsa-sheet-create-notify.md)
</dt> <dt>

[**дсобжектнамес**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**дсобжект**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> </dl>

 

 





