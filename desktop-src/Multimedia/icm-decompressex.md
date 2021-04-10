---
title: Сообщение ICM_DECOMPRESSEX (VFW. h)
description: Сообщение ICM \_ декомпрессекс уведомляет драйвер сжатия видео о необходимости распаковать кадр данных непосредственно на экран, распаковать его со слоем DIB или распаковать изображения, описанные в исходных и целевых прямоугольниках.
ms.assetid: ed253280-c246-4e86-91f1-ad1e1132d732
keywords:
- ICM_DECOMPRESSEX сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d33451547bc598250a97e73682712e157aa13a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071893"
---
# <a name="icm_decompressex-message"></a>\_Сообщение ICM декомпрессекс

Сообщение **ICM \_ декомпрессекс** уведомляет драйвер сжатия видео о необходимости распаковать кадр данных непосредственно на экран, распаковать его со слоем DIB или распаковать изображения, описанные в исходных и целевых прямоугольниках.


```C++
ICM_DECOMPRESSEX 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*икдекс*
</dt> <dd>

Указатель на структуру [**икдекомпрессекс**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Размер [**икдекомпрессекс**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

Это сообщение похоже на [**\_ распаковку ICM**](icm-decompress.md) , за исключением того, что в нем используется структура [**икдекомпрессекс**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) для определения сведений о распаковке.

Если требуется, чтобы драйвер распаковать данные непосредственно на экране, отправьте сообщение [**ICM \_ Draw**](icm-draw.md) .

Драйвер возвращает ошибку, если это сообщение получено до сообщения [**ICM \_ декомпрессекс \_ Begin**](icm-decompressex-begin.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                       |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Диспетчер сжатия видео](video-compression-manager.md)
</dt> <dt>

[Сообщения о сжатии видео](video-compression-messages.md)
</dt> </dl>

 

 





