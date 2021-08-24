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
ms.openlocfilehash: 00d419d05a21c9328d29c23ee4c6475254cc6635594cc20e989144361caab3dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443284"
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

Тип: **пкуидлист \_ Относительный \***

Адрес переменной ПИДЛ для получения перевода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

По завершении необходимо освободить возвращенный ПИДЛ с [**илфри**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




