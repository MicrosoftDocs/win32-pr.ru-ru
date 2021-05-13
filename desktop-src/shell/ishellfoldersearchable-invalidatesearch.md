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
ms.openlocfilehash: 43d76c6a27b301a61474b8028af16e5e540cf2ce
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841695"
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

Тип: **DWORD \***

Флаги в настоящее время не определены; Задайте **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Если папка поиска становится недействительной, она может выполнить очистку всех используемых ресурсов. Метод **ишеллфолдерсеарчабле:: инвалидатесеарч** может привести к отмене асинхронного поиска и приведет к выходу окончательного выпуска объекта интерфейса [**ишеллфолдерсеарчаблекаллбакк**](ishellfoldersearchablecallback.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




