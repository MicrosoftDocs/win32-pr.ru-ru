---
description: Метод Жетграупкомпрессор извлекает фильтр сжатия для указанной группы.
ms.assetid: 9d71e659-7abb-48c6-b9bd-5239560dc150
title: 'Метод Исмартрендеренгине:: Жетграупкомпрессор (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.GetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd866daa225ab398e1a578aa8d21e73bad15e96d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675614"
---
# <a name="ismartrenderenginegetgroupcompressor-method"></a>Метод Исмартрендеренгине:: Жетграупкомпрессор

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetGroupCompressor`Метод извлекает фильтр сжатия для указанной группы.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetGroupCompressor(
   long        Group,
   IBaseFilter **pCompressor
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Группа* 
</dt> <dd>

Отсчитываемый от нуля индекс группы.

</dd> <dt>

*пкомпрессор* 
</dt> <dd>

Получает указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) фильтра сжатия. Если фильтр сжатия отсутствует, он получает значение **null** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Этот метод используется для задания свойств фильтра сжатия, например частоты ключевых кадров. Вызовите этот метод после вызова [**ирендеренгине:: коннектфронтенд**](irenderengine-connectfrontend.md), но перед отрисовкой проекта. Затем запросите выходной ПИН-код фильтра сжатия для интерфейса [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) , который содержит методы для настройки параметров сжатия. Выпустите интерфейс по завершении. При внесении последующих изменений на временную шкалу вызовите **коннектфронтенд**, а затем снова вызовите **жетграупкомпрессор** , чтобы сбросить параметры сжатия.

При возврате, если значение \* *Пкомпрессор* не **равно NULL**, то интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) имеет необработанный счетчик ссылок. Не забудьте освободить интерфейс по завершении его использования.

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Исмартрендеренгине**](ismartrenderengine.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




