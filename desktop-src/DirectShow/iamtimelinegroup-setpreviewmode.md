---
description: Метод Сетпревиевмоде задает режим предварительного просмотра для группы.
ms.assetid: 40b7e9ac-30b3-454e-82ac-10ac99f1b86f
title: 'Метод Иамтимелинеграуп:: Сетпревиевмоде (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f4c53372066ec28f3782fe53148eaba99489187c3be9b9ccf73195a7b1e6da9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756314"
---
# <a name="iamtimelinegroupsetpreviewmode-method"></a>Метод Иамтимелинеграуп:: Сетпревиевмоде

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

Метод Сетпревиевмоде задает режим предварительного просмотра для группы.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetPreviewMode(
   BOOL fPreview
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фпревиев* 
</dt> <dd>

Режим предварительного просмотра. Если **значение — true**, группа находится в режиме предварительного просмотра. Если задано **значение false**, группа находится в режиме разработки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

В режиме предварительного просмотра фреймы удаляются во время незначительного эффекта или переходов для синхронизации видео с аудио. В результате видео может выглядеть прерывисто. В режиме разработки отображается каждый кадр. Режим разработки подходит для записи файлов. При предварительном просмотре видео может быть не синхронизировано с звуковым экраном.

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Иамтимелинеграуп**](iamtimelinegroup.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




