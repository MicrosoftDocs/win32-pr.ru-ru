---
description: 'Уведомляет объект обратного вызова сайта контейнера. Используется только в том случае, если IObjectWithSite:: SetSite не поддерживается и используется Шкреатешеллфолдервиевекс. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
ms.assetid: a4aa40f8-1d98-4686-86e2-87280e470aac
title: Сообщение SFVM_SETISFV (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83021f1d6d52286f08e8ec7bd51bbaa806c17c7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986100"
---
# <a name="sfvm_setisfv-message"></a>\_Сообщение сфвм сетисфв

\[Это уведомление поддерживается в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003. В последующих версиях Windows она может не поддерживаться.\]

Уведомляет объект обратного вызова сайта контейнера. Используется только в том случае, если [**IObjectWithSite:: SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) не поддерживается и используется [**шкреатешеллфолдервиевекс**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) . Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_SETISFV
    lParam = (LPARAM)(IUnknown*) site;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*сайт* \[ окне\]
</dt> <dd>

Указатель на интерфейс [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) сайта контейнера.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
