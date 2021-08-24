---
description: Метод Сетпропс задает для свойств целевого объекта соответствующее состояние в течение указанного времени.
ms.assetid: 65e701c9-d3a1-4396-9cba-a7830757701f
title: 'Метод Ипропертисеттер:: Сетпропс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b3b5a1832897b52d21c57e26595b7d66c4fc9a53f2bcbee0090c53d00f8fe832
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767214"
---
# <a name="ipropertysettersetprops-method"></a>Метод Ипропертисеттер:: Сетпропс

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetProps`Метод задает для свойств целевого объекта соответствующее состояние в течение указанного времени.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetProps(
  [in] IUnknown       *pTarget,
  [in] REFERENCE_TIME rtNow
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птаржет* \[ окне\]
</dt> <dd>

Указатель на целевой объект, для которого необходимо задать свойства.

</dd> <dt>

*ртнов* \[ окне\]
</dt> <dd>

Время, когда необходимо задать свойства, в единицах измерения 100-наносекундных или – 1, чтобы задать статические свойства (которые не меняются со временем).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Этот метод вызывается DES для задания свойств перехода или воздействия. Приложение не будет вызывать этот метод обычным образом.

Объект, указанный параметром *птаржет* , должен реализовывать интерфейс **IDispatch** .

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

[**Интерфейс Ипропертисеттер**](ipropertysetter.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




