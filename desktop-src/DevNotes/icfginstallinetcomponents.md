---
description: Устанавливает указанные системные компоненты.
ms.assetid: f4b7b8e5-b392-4208-9f56-b343974e05ff
title: Функция Икфгинсталлинеткомпонентс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgInstallInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: 649b1fa73bcdd83d7fc01d5a4df9a198168a3f1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648701"
---
# <a name="icfginstallinetcomponents-function"></a>Функция Икфгинсталлинеткомпонентс

Устанавливает указанные системные компоненты.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IcfgInstallInetComponents(
   HWND   hwndParent,
   DWORD  dwfOptions,
   LPBOOL lpfNeedsRestart
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хвндпарент* 
</dt> <dd>

Маркер родительского окна.

</dd> <dt>

*двфоптионс* 
</dt> <dd>

Сочетание следующих флагов, управляющих установкой и настройкой.



| Значение                                                                                                                                                                                                                                  | Значение                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**Икфг \_ ИНСТАЛЛМАИЛ**</dt> <dt>0x00000004</dt> </dl> | Установите Exchange и Internet Mail.<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**Икфг \_ ИНСТАЛЛРАС**</dt> <dt>0x00000002</dt> </dl>    | Установите RAS (при необходимости).<br/>            |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**Икфг \_ ИНСТАЛЛТКП**</dt> <dt>0x00000001</dt> </dl>    | Установите TCP/IP (при необходимости).<br/>         |



 

</dd> <dt>

*лпфнидсрестарт* 
</dt> <dd>

Если это значение не **равно NULL**, то при возврате произойдет **значение true** , только если для завершения установки необходимо перезапустить Windows.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Если ошибки не возникают, возвращается код **\_ успешного выполнения ошибки** .

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
