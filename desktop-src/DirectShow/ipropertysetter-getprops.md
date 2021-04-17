---
description: Метод PROPS извлекает свойства, заданные для этого объекта, с соответствующими значениями.
ms.assetid: 2a2ac262-f5a4-4bbe-9cd2-aa7c7d359917
title: Метод Ипропертисеттер::-PROPS (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.GetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f512ce672cbbaca6556ad644f21c684130eb28e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685217"
---
# <a name="ipropertysettergetprops-method"></a>Метод Ипропертисеттер:: Props

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetProps`Метод получает свойства, заданные для этого объекта, с соответствующими значениями.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetProps(
  [out] LONG         *pcParams,
  [out] DEXTER_PARAM **paParam,
  [out] DEXTER_VALUE **paValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкпарамс* \[ заполняет\]
</dt> <dd>

Получает количество структур, возвращенных в *папарам*.

</dd> <dt>

*папарам* \[ заполняет\]
</dt> <dd>

Адрес указателя на массив структур [**\_ param Декстер**](dexter-param.md) .

</dd> <dt>

*павалуе* \[ заполняет\]
</dt> <dd>

Адрес указателя на массив структур [**\_ значений Декстер**](dexter-value.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Для каждого свойства, возвращаемого в *папарам*, элемент **nзначения** указывает количество структур [**Декстер \_ значений**](dexter-value.md) , связанных со свойством. Эти пары возвращаются в возрастающем порядке по времени для каждого свойства.

По завершении использования возвращенных структур вызовите метод [**ипропертисеттер:: фрипропс**](ipropertysetter-freeprops.md) , чтобы освободить ресурсы, выделенные этим методом.

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

## <a name="examples"></a>Примеры

В следующем примере кода показано, как выполнить итерацию всех значений в экземпляре метода задания свойства:


```C++
IPropertySetter *pSetter = NULL;
// Get a valid IPropertySetter pointer (not shown).

DEXTER_PARAM *pParam;
DEXTER_VALUE *pValue;
LONG count;

hr = pSetter->GetProps(&count, &pParam, &pValue);

LONG num = 0;
for (LONG i = 0; i < count; i++)
{
    for (LONG j = 0; j < pParam[i].nValues; j++)
    {
        // pValue[num] is the next value in the sequence for pParam[i]
    }
    num += pParam[i].nValues;
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипропертисеттер**](ipropertysetter.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




