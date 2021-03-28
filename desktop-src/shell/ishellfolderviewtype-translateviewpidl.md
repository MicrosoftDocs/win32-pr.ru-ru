---
description: Восстанавливает указатель на список идентификаторов элементов (ПИДЛ) из одного иерархического представления папки оболочки в другое представление.
title: 'Метод Ишеллфолдервиевтипе:: Транслатевиевпидл'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.TranslateViewPidl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b7fa6c4-3d02-44ed-b63d-80a799e4017a
ms.openlocfilehash: 75876e5088c610c1f9f02ba9374db5cea4a6023c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543106"
---
# <a name="ishellfolderviewtypetranslateviewpidl-method"></a>Метод Ишеллфолдервиевтипе:: Транслатевиевпидл

Восстанавливает указатель на список идентификаторов элементов (ПИДЛ) из одного иерархического представления папки оболочки в другое представление.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT TranslateViewPidl(
  [in] PCUIDLIST_RELATIVE pidl,
  [in] PCUIDLIST_RELATIVE pidlView,
  [in] PCUIDLIST_RELATIVE *ppidlOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Пидл* \[ окне\]
</dt> <dd>

Тип: **пкуидлист \_ относительный**

Массив идентификаторов элементов относительно корневой папки.

</dd> <dt>

*пидлвиев* \[ окне\]
</dt> <dd>

Тип: **пкуидлист \_ относительный**

Специальная ПИДЛ представления.

</dd> <dt>

*ппидлаут* \[ окне\]
</dt> <dd>

Тип: **пкуидлист \_ Относительный \** _

Адрес переменной ПИДЛ для получения перевода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Примечания

По завершении необходимо освободить возвращенный ПИДЛ с [**илфри**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




