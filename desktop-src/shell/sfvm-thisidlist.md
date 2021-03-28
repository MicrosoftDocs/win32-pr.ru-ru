---
description: СФВМ \_ сисидлист может быть изменен или недоступен.
ms.assetid: 488f696d-aa71-4727-bbd2-c99e7d245d85
title: Сообщение SFVM_THISIDLIST (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86e24199e5adbb895c8d1d5fc36bfff0c109bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818617"
---
# <a name="sfvm_thisidlist-message"></a>\_Сообщение сфвм сисидлист

\[**Сфвм \_ СИСИДЛИСТ** доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен.\]

Позволяет объекту обратного вызова указать указатель представления на список идентификаторов элементов (ПИДЛ). Используется, только если не удалось выполнить [**иперсистидлист:: сетидлист**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) и [**IPersistFolder2:: жеткурфолдер**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) . Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_THISIDLIST
    lParam = (LPARAM)(LPITEMIDLIST*) pidl;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Пидл* \[ заполняет\]
</dt> <dd>

Адрес ПИДЛ представления.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                |
| Окончание поддержки клиента<br/>    | Windows XP с пакетом обновления 2 (SP2)<br/>                                                      |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
