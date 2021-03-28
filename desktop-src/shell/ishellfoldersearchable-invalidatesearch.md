---
description: Делает этот указатель на список идентификаторов элементов (ПИДЛ) недопустимой частью папки оболочки.
title: 'Метод Ишеллфолдерсеарчабле:: Инвалидатесеарч'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.InvalidateSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6985a299-8547-4db4-99f9-d46dafe4789b
ms.openlocfilehash: 36c1de0a606fdfddbe8eb74b5cc6c20cdda8e983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263349"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a>Метод Ишеллфолдерсеарчабле:: Инвалидатесеарч

Делает этот указатель на список идентификаторов элементов (ПИДЛ) недопустимой частью папки оболочки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пидлсеарч* \[ окне\]
</dt> <dd>

Тип: **лпЦитемидлист**

Указатель на структуру [**итемидлист**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) для папки поиска.

</dd> <dt>

*пдвфлагс* \[ окне\]
</dt> <dd>

Введите: **DWORD \** _

Флаги в настоящее время не определены; Задайте значение _ * NULL * *.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Примечания

Если папка поиска становится недействительной, она может выполнить очистку всех используемых ресурсов. Метод **ишеллфолдерсеарчабле:: инвалидатесеарч** может привести к отмене асинхронного поиска и приведет к выходу окончательного выпуска объекта интерфейса [**ишеллфолдерсеарчаблекаллбакк**](ishellfoldersearchablecallback.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




