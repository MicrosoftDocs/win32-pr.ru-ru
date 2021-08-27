---
description: Задает текущий компьютер воспроизведения для указанного журнала графики.
MS-HAID: vspixengine.IPixEngine2\_SetPlaybackMachine\_BSTR\_BOOL\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine2:: Сетплайбаккмачине'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 181EE044-1FC4-484B-AE63-C33BC627C3B7
api_name:
- IPixEngine2.SetPlaybackMachine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c1c4ca173b9ccef80d6f9d89f1829f7170459e90
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628180"
---
# <a name="span-idvspixengineipixengine2_setplaybackmachine_bstr_bool_bstrspanipixengine2setplaybackmachine-method"></a><span id="vspixengine.ipixengine2_setplaybackmachine_bstr_bool_bstr"></span>Метод IPixEngine2:: Сетплайбаккмачине

Задает текущий компьютер воспроизведения для указанного журнала графики.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetPlaybackMachine(
   BSTR logFile,
   BOOL bUseAuthentication,
   BSTR machine
);
```

## <a name="parameters"></a>Параметры

*logFile*   
Строка COM, контианинг имя журнала графики.

*бусеаусентикатион*   
значение true, чтобы использовать проверку подлинности; в противном случае — значение false.

*машине*   
Строка COM, содержащая имя компьютера воспроизведения.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**IPixEngine2**](/windows/desktop/direct3dtools/ipixengine2)

 

 
