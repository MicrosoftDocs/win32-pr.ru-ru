---
description: 'Уведомляет объект обратного вызова сайта контейнера. Используется только в том случае, если IObjectWithSite:: SetSite не поддерживается и используется Шкреатешеллфолдервиевекс. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
ms.assetid: a4aa40f8-1d98-4686-86e2-87280e470aac
title: Сообщение SFVM_SETISFV (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6d9ad3e9b1b8302089da8a59a8d5502a04392da77c6fc5276725b144efa026
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660804"
---
# <a name="sfvm_setisfv-message"></a>\_Сообщение сфвм сетисфв

\[это уведомление поддерживается в Windows XP с пакетом обновления 2 (sp2) и Windows Server 2003. В последующих версиях Windows он может не поддерживаться.\]

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
