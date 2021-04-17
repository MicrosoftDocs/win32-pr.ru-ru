---
description: Определяет, установлены ли компоненты, отмеченные в параметрах, в системе.
ms.assetid: 5fda917a-9c4b-42a3-8f79-9c609f56eb9f
title: Функция Икфгнидинеткомпонентс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgNeedInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: c851ed7d5610d96af636afb60114a51be9c711f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657741"
---
# <a name="icfgneedinetcomponents-function"></a>Функция Икфгнидинеткомпонентс

Определяет, установлены ли компоненты, отмеченные в параметрах, в системе.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IcfgNeedInetComponents(
   DWORD  dwfOptions,
   LPBOOL lpfNeedComponents
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двфоптионс* 
</dt> <dd>

Сочетание следующих флагов, указывающих, какие компоненты следует обнаружить из следующего списка.



| Значение                                                                                                                                                                                                                                  | Значение                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**Икфг \_ ИНСТАЛЛМАИЛ**</dt> <dt>0x00000004</dt> </dl> | Требуется ли Exchange или Internet Mail?<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**Икфг \_ ИНСТАЛЛРАС**</dt> <dt>0x00000002</dt> </dl>    | Требуется ли RAS?<br/>                       |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**Икфг \_ ИНСТАЛЛТКП**</dt> <dt>0x00000001</dt> </dl>    | Требуется ли TCP/IP?<br/>                    |



 

</dd> <dt>

*лпфнидкомпонентс* 
</dt> <dd>

Если это значение не **равно NULL**, возвращается **значение true** , если один или несколько компонентов не установлены в системе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Если ошибки не возникают, возвращается код **\_ успешного выполнения ошибки** .

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
