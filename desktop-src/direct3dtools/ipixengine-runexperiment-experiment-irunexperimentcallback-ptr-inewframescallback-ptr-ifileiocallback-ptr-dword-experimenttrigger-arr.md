---
description: Выполняет эксперимент.
MS-HAID: vspixengine.IPixEngine\_RunExperiment\_Experiment\_IRunExperimentCallback\_ptr\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_DWORD\_ExperimentTrigger\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипиксенгине:: Рунексперимент'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A2EEC278-C074-44B3-94DC-E2D9DC770576
api_name:
- IPixEngine.RunExperiment
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 94698ae1f90bc9e7b242672e93117cfd48f8462cc047b676cadadc9832739afa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741934"
---
# <a name="span-idvspixengineipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arrspanipixenginerunexperiment-method"></a><span id="vspixengine.ipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arr"></span>Метод Ипиксенгине:: Рунексперимент

Выполняет эксперимент.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RunExperiment(
   Experiment               experiment,
   IRunExperimentCallback * pRequestCallback,
   INewFramesCallback*      callbacks,
   IFileIOCallback*         pFileIOCallback,
   DWORD                    triggersCount,
   ExperimentTrigger []     count4_triggersBuffer
);
```

## <a name="parameters"></a>Параметры

*немного*   
Описывает эксперимент, который необходимо выполнить.

*прекуесткаллбакк*   
Адрес функции, используемой для уведомления узла о том, что модуль начал эксперимент.

*обратные вызовы*   
Адрес функции, используемой для уведомления узла о том, что были записаны новые кадры.

*пфилеиокаллбакк*   
Адрес функции, используемой для уведомления узла об ошибках ввода-вывода в файле во время синтаксического анализа.

*тригжерскаунт*   
Число триггеров в эксперименте.

*count4 \_ тригжерсбуффер*   
Запись триггеров.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ипиксенгине**](/windows/desktop/direct3dtools/ipixengine)

 

 
