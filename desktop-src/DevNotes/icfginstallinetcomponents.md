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
ms.openlocfilehash: 7708dd065c066ce3e9fd8e4de1044c6bc8587d2526abdf9aeac175b4387dec42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827289"
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
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**Икфг \_ ИНСТАЛЛМАИЛ**</dt> <dt>0x00000004</dt> </dl> | установите Exchange и Internet mail.<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**Икфг \_ ИНСТАЛЛРАС**</dt> <dt>0x00000002</dt> </dl>    | Установите RAS (при необходимости).<br/>            |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**Икфг \_ ИНСТАЛЛТКП**</dt> <dt>0x00000001</dt> </dl>    | Установите TCP/IP (при необходимости).<br/>         |



 

</dd> <dt>

*лпфнидсрестарт* 
</dt> <dd>

если это значение не **равно NULL**, то возвращается значение **TRUE** , только если для завершения установки необходимо перезапустить Windows.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Если ошибки не возникают, возвращается код **\_ успешного выполнения ошибки** .

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
