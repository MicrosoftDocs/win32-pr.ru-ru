---
description: Используется для определения, следует ли отображать этот параметр общей папки в веб-представлении.
title: Функция CanShareFolderW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CanShareFolderW
- CanShareFolderW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.assetid: 5fd28a14-53e7-4016-9c49-9bb14ce7808b
ms.openlocfilehash: 7013c6ae825c34ae7d2dd7b9d507eac1e52c8d4e3a27182e5297e72ef13b4d9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032872"
---
# <a name="cansharefolderw-function"></a>Функция CanShareFolderW

\[эта функция доступна в Windows XP с пакетом обновления 2 (sp2) и Windows Server 2003. Он может быть изменен или недоступен в последующих версиях Windows.\]

Используется для определения, следует ли отображать **этот параметр общей папки** в веб-представлении.

## <a name="syntax"></a>Синтаксис


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псзпас* \[ окне\]
</dt> <dd>

Тип: **лпквстр**

Указатель на строку, указывающую путь к проверяемой папке.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **стдапи**

К возвращаемым значениям относятся следующие.



| Возвращаемый код и значение                                                                        | Описание                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>     | Путь, на который указывает *псзпас* , указывает папку, к которой можно предоставить общий доступ.<br/>    |
| <dl> <dt>**S \_ false**</dt> </dl>  | Путь, на который указывает *псзпас* , указывает папку, к которой нельзя предоставить общий доступ.<br/> |
| <dl> <dt>Ошибка HRESULT</dt> </dl> | Произошла ошибка.<br/>                                                     |



 

## <a name="remarks"></a>Remarks

Эта функция не имеет связанного LIB файла. Для его использования необходимо использовать [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Каншарефолдерв** (Юникод)<br/>                                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[**шовшарефолдеруи**](./showsharefolderui.md)
</dt> </dl>

 

 
