---
description: Начинает поиск указанной строки поиска.
ms.assetid: 6ecad03c-e8e0-45ba-8def-b55a029992f2
title: 'Метод Ишеллфолдерсеарчабле:: FindString (MMC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.FindString
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3e256329bc235f7fe5a0428ba33710fa6b838f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810948"
---
# <a name="ishellfoldersearchablefindstring-method"></a>Метод Ишеллфолдерсеарчабле:: FindString

Начинает поиск указанной строки поиска.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT FindString(
  [in]  LPCWSTR      pwszTarget,
  [in]  DWORD        *pdwFlags,
  [in]  IUnknown     *punkOnAsyncSearch,
  [out] LPITEMIDLIST ppidlOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвсзтаржет* \[ окне\]
</dt> <dd>

Тип: **лпквстр**

Указатель на строку, указывающую ключевое слово поиска.

</dd> <dt>

*пдвфлагс* \[ окне\]
</dt> <dd>

Введите: **DWORD \** _

Флаги в настоящее время не определены; Задайте значение _ * NULL * *.

</dd> <dt>

*пунконасинксеарч* \[ окне\]
</dt> <dd>

Тип: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Указатель на объект типа [_ *IUnknown* *](/windows/win32/api/unknwn/nn-unknwn-iunknown). Этот объект должен поддерживать интерфейс [**ишеллфолдерсеарчаблекаллбакк**](ishellfoldersearchablecallback.md) . Если обратный вызов не требуется, задайте значение **null** .

</dd> <dt>

*ппидлаут* \[ заполняет\]
</dt> <dd>

Тип: **лпитемидлист**

Указатель на структуру [**итемидлист**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) для папки поиска.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Заголовок<br/>                   | <dl> <dt>MMC. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
