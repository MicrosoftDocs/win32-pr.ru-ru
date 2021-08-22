---
description: Указывает, как выделить поверхности Microsoft Direct3D 11 для образцов мультимедиа.
ms.assetid: E9A415FA-74BF-4822-BB0E-D8AAA7D73664
title: Атрибут MF_SA_D3D11_USAGE (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7364b9777d94baa1a6c25aead6631ad6b11dcddc12db83698da04affebe0fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663954"
---
# <a name="mf_sa_d3d11_usage-attribute"></a>\_ \_ Атрибут использования D3D11 SA для MF \_

Указывает, как выделить поверхности Microsoft Direct3D 11 для образцов мультимедиа. Использование показывает, доступен ли образец для ЦП или GPU.

## <a name="data-type"></a>Тип данных

**D3D11 \_ Использование** хранится как **UINT32**

## <a name="remarks"></a>Remarks

Значение этого атрибута является значением [**\_ использования D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) .

### <a name="microsoft-media-foundation-transforms"></a>Преобразования Microsoft Media Foundation

В этом контексте атрибут применяется только в том случае, если преобразование Microsoft Media Foundation (MFT) возвращает **true** для атрибута [MF \_ SA D3D11 с \_ \_ поддержкой](mf-sa-d3d11-aware.md) .

Если файл MFT поддерживает Direct3D 11, этот атрибут предоставляет указание для MFT при выделении поверхностей Microsoft Direct3D для вывода. Задайте атрибут следующим образом:

1.  Вызовите [**имфтрансформ:: жетаутпутстреаматтрибутес**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) , чтобы получить хранилище атрибутов MFT.
2.  Вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

Конвейер Media Foundation задает атрибут перед запуском потоковой передачи. MFT должна попытаться учитывать параметр при выделении поверхностей. Если это невозможно, MFT может игнорировать атрибут вместо сбоя выделения.

Кроме того, если в MFT требуются поверхности Direct3D для входных данных, он может предоставить этот атрибут как подсказку для выделения поверхностей ввода. Запросите атрибут следующим образом:

1.  Вызовите метод [**имфтрансформ:: жетинпутстреаматтрибутес**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) , чтобы получить атрибуты входного потока.
2.  Вызовите [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

### <a name="sample-allocator"></a>Выборка распределителя

Этот атрибут можно задать в примере распределителя видео в методе [**имфвидеосамплеаллокаторекс:: инитиализесамплеаллокаторекс**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                              |
| Заголовок<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
