---
description: Шеллфолдервиев. Попупитеммену — создает контекстное меню для указанного элемента и возвращает выбранную командную строку.
title: Шеллфолдервиев. Попупитеммену, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.PopupItemMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1610d91e-87c3-4ba5-9147-1595eddb2c3a
ms.openlocfilehash: cb862ba159f55d3ab82495ddeb32a87f3ce1901b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083392"
---
# <a name="shellfolderviewpopupitemmenu-method"></a>Шеллфолдервиев. Попупитеммену, метод

Создает контекстное меню для указанного элемента и возвращает выбранную командную строку.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*витем* \[ окне\]
</dt> <dd>

Тип: **Variant**

Объект [**FolderItem**](folderitem.md) , для которого будет создано контекстное меню.

</dd> <dt>

*VX* \[ в, необязательно\]
</dt> <dd>

Тип: **Variant**

Горизонтальное расположение меню в экранных координатах.

</dd> <dt>

*Ви* \[ в необязательное\]
</dt> <dd>

Тип: **Variant**

Вертикальное расположение меню в экранных координатах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***

**Строка** , получающая командную строку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 
