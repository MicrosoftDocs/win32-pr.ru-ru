---
description: 'Позволяет объекту обратного вызова предоставлять сведения о зоне Интернета. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
ms.assetid: 6fae7925-b1be-4270-9318-7fa517563dad
title: Сообщение SFVM_GETZONE (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5586188aeab6a054e22e4b242039beaae1ce390d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546935"
---
# <a name="sfvm_getzone-message"></a>Сообщение СФВМ в \_ зоне

\[Это уведомление поддерживается в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003. В последующих версиях Windows она может не поддерживаться.\]

Позволяет объекту обратного вызова предоставлять сведения о зоне Интернета. Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETZONE
    lParam = (LPARAM)(DWORD*) zone;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*зона* \[ заполняет\]
</dt> <dd>

Одно из следующих значений, указывающее зону Интернета. Эти значения составляют перечисление [**урлзоне**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) , определенное в Urlmon. h.

<dt>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**УРЛЗОНЕ \_ локальный \_ компьютер**


</dt> <dd>

Зона, используемая для содержимого, уже расположенного на локальном компьютере пользователя. Эта зона не предоставляется пользовательским интерфейсом.

</dd> <dt>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**\_интрасеть урлзоне**


</dt> <dd>

Зона, используемая для содержимого, обнаруженного в интрасети.

</dd> <dt>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**УРЛЗОНЕ \_ доверенный**


</dt> <dd>

Зона, используемая для доверенных веб-сайтов в Интернете.

</dd> <dt>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**УРЛЗОНЕ \_ Интернет**


</dt> <dd>

Зона, используемая для большей части содержимого в Интернете.

</dd> <dt>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**УРЛЗОНЕ \_ без доверия**


</dt> <dd>

Зона, используемая для веб-сайтов, которые не являются доверенными.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
