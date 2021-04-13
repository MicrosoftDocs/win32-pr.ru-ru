---
description: Проверяет один файл каталога, используя стандартную политику подписывания кода операционной системы, например подписывание драйверов.
ms.assetid: 1e2a18a5-506e-46a8-9309-666bec92182d
title: Функция Псетупверификаталогфиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupVerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 3de792ae6738277d2ab7cb21d8be7f4c5ecfb573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647997"
---
# <a name="psetupverifycatalogfile-function"></a>Функция Псетупверификаталогфиле

\[Эта функция больше не поддерживается корпорацией Майкрософт. Для INF-файла (Установка устройства) разработчики должны использовать **сетупверифинффиле**. Чтобы проверить каталог, не основанный на INF, используйте **WinVerifyTrust**.\]

Проверяет один файл каталога, используя стандартную политику подписывания кода операционной системы, например подписывание драйверов.

## <a name="syntax"></a>Синтаксис


```C++
DWORD pSetupVerifyCatalogFile(
  _In_ LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Каталогфуллпас* \[ окне\]
</dt> <dd>

Полный путь к файлу каталога, который необходимо проверить.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, возвращается **сообщение об \_ ошибке**; в противном случае возвращается ошибка от [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сетупверифинффиле**](/windows/win32/api/setupapi/nf-setupapi-setupverifyinffilea)
</dt> <dt>

[**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)
</dt> </dl>

 

 
