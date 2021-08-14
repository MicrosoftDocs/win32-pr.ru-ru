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
ms.openlocfilehash: 947cda4094491702fa0f847e6a8abd4fed7bcbe9bd3504c5f8aec2097b0d6b8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220940"
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

Тип: **DWORD \***

Флаги в настоящее время не определены; Задайте **значение NULL**.

</dd> <dt>

*пунконасинксеарч* \[ окне\]
</dt> <dd>

Тип: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Указатель на объект типа [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Этот объект должен поддерживать интерфейс [**ишеллфолдерсеарчаблекаллбакк**](ishellfoldersearchablecallback.md) . Если обратный вызов не требуется, задайте значение **null** .

</dd> <dt>

*ппидлаут* \[ заполняет\]
</dt> <dd>

Тип: **лпитемидлист**

Указатель на структуру [**итемидлист**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) для папки поиска.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Заголовок<br/>                   | <dl> <dt>MMC. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
