---
description: Проверяет доступность указанного расширения на компьютере и может ли он использоваться методом IWiaItem2::-Extension.
ms.assetid: 672f6418-4ce3-4570-a412-fe639c9f5eb8
title: 'Метод IWiaItem2:: Чеккекстенсион (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CheckExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 50240fbf10155fae555c6cd2e30bf8c86c571b8d52b86e02eab9f5bb11ac17ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965583"
---
# <a name="iwiaitem2checkextension-method"></a>Метод IWiaItem2:: Чеккекстенсион

Проверяет доступность указанного расширения на компьютере и может ли он использоваться методом [**IWiaItem2::-Extension**](-wia-iwiaitem2-getextension.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CheckExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] BOOL   *pbExtensionExists
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лфлагс* \[ окне\]
</dt> <dd>

Тип: **Long**

В настоящее время не используется. Значение должно быть равно нулю.

</dd> <dt>

*bstrName* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Указывает имя расширения.

</dd> <dt>

*риидекстенсионинтерфаце* \[ окне\]
</dt> <dd>

Тип: **рефиид**

В настоящее время не используется.

</dd> <dt>

*пбекстенсионексистс* \[ заполняет\]
</dt> <dd>

Тип: **bool \*** .

Получает указатель на **логическое** значение.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**ISFALSE**


</dt> <dd>

Указанное расширение недоступно.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**УСЛОВИЯ**


</dt> <dd>

Указанное расширение доступно.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

С помощью этого метода приложения могут проверить, доступно ли расширение, до вызова метода [**IWiaItem2::-Extension**](-wia-iwiaitem2-getextension.md) . Кроме того, приложение может проверить, какие расширения доступны без совместного создания, а затем решить, какой из них следует использовать.

## <a name="examples"></a>Примеры

Чеккимгфилтер проверяет, имеет ли драйвер фильтр обработки изображений. Перед вызовом компонента предварительной версии приложение должно убедиться, что драйвер имеет фильтр обработки изображений.


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   return hr;

}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




