---
description: Метод Сетресизергуид задает идентификатор CLSID пользовательского фильтра изменения размера видео.
ms.assetid: 709a6e7f-64ae-406d-bb6d-29f6c65b63a8
title: 'Метод IRenderEngine2:: Сетресизергуид (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2.SetResizerGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 864053c2c5def6ef1b23ca2c2ee712664e132079
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679842"
---
# <a name="irenderengine2setresizerguid-method"></a>Метод IRenderEngine2:: Сетресизергуид

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetResizerGUID`Метод задает идентификатор CLSID пользовательского фильтра изменения размера видео. Вызовите этот метод, чтобы заменить применяемый по умолчанию фильтр изменения размера, используемый службами редактирования DirectShow. Фильтр должен быть зарегистрирован в системе пользователя как COM-объект и должен поддерживать интерфейс [**иресизе**](iresize.md) .

Вызовите этот метод перед вызовом [**ирендеренгине:: коннектфронтенд**](irenderengine-connectfrontend.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetResizerGUID(
  [in] GUID ResizerGuid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ресизергуид* \[ окне\]
</dt> <dd>

Идентификатор CLSID фильтра.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Чтобы вернуться к измененному по умолчанию размеру DES, используйте следующий идентификатор CLSID:


```C++
// {F97B8A60-31AD-11CF-B2DE-00DD01101B85}
DEFINE_GUID(CLSID_Resize, 
0xF97B8A60, 0x31AD, 0x11CF, 0xB2, 0xDE, 0x00, 0xDD, 0x01, 0x10, 0x1B, 0x85);
```



> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | DirectX 9,0 или более поздней версии<br/>                                                         |
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> <dt>

[**Интерфейс IRenderEngine2**](irenderengine2.md)
</dt> </dl>

 

 




