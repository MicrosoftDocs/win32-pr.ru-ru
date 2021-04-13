---
title: Сообщение ICM_DRAW_SUGGESTFORMAT (VFW. h)
description: Сообщение ICM \_ Draw \_ сугжестформат запрашивает драйвер подготовки к просмотру, чтобы предложить формат, который может нарисоваться в распакованном формате.
ms.assetid: e3e97790-dbd1-4436-9830-5218ae1f949b
keywords:
- ICM_DRAW_SUGGESTFORMAT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_SUGGESTFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97c8782b16336427b3832f36b5a06987399df1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489594"
---
# <a name="icm_draw_suggestformat-message"></a>\_Сообщение ICM Draw \_ сугжестформат

Сообщение **ICM \_ Draw \_ сугжестформат** запрашивает драйвер подготовки к просмотру, чтобы предложить формат, который может нарисоваться в распакованном формате.


```C++
ICM_DRAW_SUGGESTFORMAT 
wParam = (DWORD_PTR) (LPVOID) &icdrwSuggest; 
lParam = sizeof(ICDRAWSUGGEST); 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*икдрвсугжест*
</dt> <dd>

Указатель на структуру [**икдравсугжест**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Размер [**икдравсугжест**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ИЦЕРР \_ ОК в случае успеха. Если элемент **лпбисугжест** структуры [**Икдравсугжест**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) имеет **значение NULL**, это сообщение возвращает объем памяти, необходимый для хранения рекомендуемого формата.

## <a name="remarks"></a>Комментарии

Драйвер должен проверить формат, указанный в элементе **лпбиин** структуры [**икдравсугжест**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) , и использовать элемент **лпбисугжест** для возврата формата, который он может нарисовать. Формат вывода должен сохранять как можно больше данных из входного формата.

При необходимости драйвер может использовать установщик, который можно установить, переданный в члене **Хикдекомпрессор** [**икдравсугжест**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) , чтобы сделать более сложными выборки. Например, если входной формат имеет 24 бита данных в формате JPEG, модуль подготовки отчетов может запросить декомпрессор, чтобы выяснить, может ли он распаковать его в формат YUV (который может быть более эффективным), прежде чем выбирать нужный формат.

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

 

 





