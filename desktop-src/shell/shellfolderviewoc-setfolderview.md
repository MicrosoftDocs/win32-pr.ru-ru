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
ms.openlocfilehash: 41a37d1b8f9874bdddd5a9593e0eade8bc0b5b92d30f8ada4ee9c6295af1d632
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968403"
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

Тип: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\***

Объект [**шеллфолдервиев**](shellfolderview.md) . Его события [**енумдоне**](shellfolderviewoc-enumdone.md) и [**SelectionChanged**](shellfolderview-selectionchanged.md) будут перенаправляться в соответствующий обработчик событий [**шеллфолдервиевок**](shellfolderviewoc-object.md) .

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



 

 
