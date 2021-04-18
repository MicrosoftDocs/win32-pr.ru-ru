---
description: Перенаправляет события указанного объекта Шеллфолдервиев в соответствующий обработчик событий Шеллфолдервиевок.
ms.assetid: 44a2a0a5-aa87-43ae-b4ea-0d301fcb8464
title: Шеллфолдервиевок. Сетфолдервиев, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC.SetFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7d331fadbd8abae62ee896caec772d84d079f88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985872"
---
# <a name="shellfolderviewocsetfolderview-method"></a>Шеллфолдервиевок. Сетфолдервиев, метод

Перенаправляет события указанного объекта [**шеллфолдервиев**](shellfolderview.md) в соответствующий обработчик событий [**шеллфолдервиевок**](shellfolderviewoc-object.md) .

## <a name="syntax"></a>Синтаксис


```JScript
iRetVal = ShellFolderViewOC.SetFolderView(
  oShellFolderView
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ошеллфолдервиев* \[ окне\]
</dt> <dd>

Тип: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) \** _

Объект [_ *шеллфолдервиев* *](shellfolderview.md) . Его события [**енумдоне**](shellfolderviewoc-enumdone.md) и [**SelectionChanged**](shellfolderview-selectionchanged.md) будут перенаправляться в соответствующий обработчик событий [**шеллфолдервиевок**](shellfolderviewoc-object.md) .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



 

 
