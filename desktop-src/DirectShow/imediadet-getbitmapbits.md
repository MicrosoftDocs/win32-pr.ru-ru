---
description: Метод Жетбитмапбитс извлекает кадр видео в указанное время носителя. Возвращаемый кадр всегда находится в 24-разрядном формате RGB.
ms.assetid: b51df9d1-9c54-41bd-b0f8-ec290525deca
title: 'Метод Имедиадет:: Жетбитмапбитс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5c4a7332580d4e9a9fece5a66d390753566fbf54c615699663256c463cb401b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792004"
---
# <a name="imediadetgetbitmapbits-method"></a>Метод Имедиадет:: Жетбитмапбитс

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetBitmapBits`Метод извлекает кадр видео в указанное время носителя. Возвращаемый кадр всегда находится в 24-разрядном формате RGB.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetBitmapBits(
   double StreamTime,
   long   *pBufferSize,
   char   *pBuffer,
   long   Width,
   long   Height
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*стреамтиме* 
</dt> <dd>

Время получения кадра видео в секундах.

</dd> <dt>

*пбуфферсизе* 
</dt> <dd>

Получает требуемый размер буфера. Если *pBuffer* имеет **значение NULL**, переменная получает размер буфера, необходимого для получения кадра. Если *pBuffer* не равно **null**, этот параметр игнорируется.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Указатель на буфер, который получает структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , за которой СЛЕДУЮТ биты DIB.

</dd> <dt>

*Width* 
</dt> <dd>

Ширина изображения видео в пикселях.

</dd> <dt>

*Height* 
</dt> <dd>

Высота изображения видео (в пикселях).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения:



| Код возврата                                                                                             | Описание                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                    | Успешно.<br/>                                                                               |
| <dl> <dt>**\_интерфейс E**</dt> </dl>           | Не удалось добавить [**образец фильтра захвата**](sample-grabber-filter.md) к диаграмме.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>           | Недостаточно памяти.<br/>                                                                   |
| <dl> <dt>**\_указатель E**</dt> </dl>               | Ошибка указателя **null** .<br/>                                                                |
| <dl> <dt>**\_непредвиденная E**</dt> </dl>            | Непредвиденная ошибка.<br/>                                                                      |
| <dl> <dt>**VFW \_ E \_ инвалидмедиатипе**</dt> </dl> | Недопустимый тип носителя.<br/>                                                                    |



 

## <a name="remarks"></a>Remarks

Перед вызовом этого метода задайте имя файла и поток, вызвав [**имедиадет::p UT \_ filename**](imediadet-put-filename.md) и [**имедиадет::p UT \_ куррентстреам**](imediadet-put-currentstream.md).

Чтобы определить необходимый размер буфера, вызовите этот метод с *pBuffer* , равным **null**. Размер возвращается в переменную, на которую указывает *пбуфферсизе*. Затем создайте буфер и снова вызовите метод с *pBuffer* , равным адресу буфера. Когда метод возвращает значение, буфер содержит структуру **битмапинфохеадер** , за которой следует точечный рисунок. Битовая карта масштабируется по измерениям, указанным в параметрах *Width* и *Height* .

Этот метод помещает средство обнаружения мультимедиа в режим захвата точечного рисунка. После вызова этого метода различные методы потоковой информации в **имедиадет** не работают, если не создать новый экземпляр детектора мультимедиа.

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="examples"></a>Примеры

В следующем коде используется `GetBitmapBits` метод для создания аппаратно-независимого точечного рисунка.


```C++
long size;
hr = pDet->GetBitmapBits(0, &size, 0, width, height);
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[size];
    if (!pBuffer)
        return E_OUTOFMEMORY;
    try {
        hr = pDet->GetBitmapBits(0, 0, pBuffer, width, height);
    }
    catch (...) {
        delete [] pBuffer;
        throw;
    }
    if (SUCCEEDED(hr))
    {
        BITMAPINFOHEADER *bmih = (BITMAPINFOHEADER*)pBuffer;
        HDC hdcDest = GetDC(0);
        
        // Find the address of the start of the image data.
        void *pData = pBuffer + sizeof(BITMAPINFOHEADER);
        
        // Note: In general a BITMAPINFOHEADER can include extra color
        // information at the end, so calculating the offset to the image
        // data is not generally correct. However, the IMediaDet interface
        // always returns an RGB-24 image with no extra color information.
        
        BITMAPINFO bmi;
        ZeroMemory(&bmi, sizeof(BITMAPINFO));
        CopyMemory(&(bmi.bmiHeader), bmih, sizeof(BITMAPINFOHEADER));
        HBITMAP hBitmap = CreateDIBitmap(hdcDest, bmih, CBM_INIT, 
            pData, &bmi, DIB_RGB_COLORS);
    }
    delete[] pBuffer;
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Имедиадет**](imediadet.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




