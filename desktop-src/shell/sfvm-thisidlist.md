---
description: СФВМ \_ сисидлист может быть изменен или недоступен.
ms.assetid: 488f696d-aa71-4727-bbd2-c99e7d245d85
title: Сообщение SFVM_THISIDLIST (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd00f1cfc2b6661dac2414f0327cab03d4c0586eb62b992b5e33f81e64565246
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968633"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                |
| Окончание поддержки клиента<br/>    | Windows XP с пакетом обновления 2 (SP2)<br/>                                                      |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
