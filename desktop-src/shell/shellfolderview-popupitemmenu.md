---
description: Создает контекстное меню для указанного элемента и возвращает выбранную командную строку.
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
ms.openlocfilehash: 513f654442361da840cb02089810c814275c5867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266171"
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

Тип: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _

Строка _ *String**, которая получает командную строку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 
