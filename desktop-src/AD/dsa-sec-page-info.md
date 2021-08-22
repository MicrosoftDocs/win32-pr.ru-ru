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
ms.openlocfilehash: 26fa3dcfb983de8e1052b319bac7c3a594e256b594847c32b553353e6caee17d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695652"
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

 

 





