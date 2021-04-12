---
description: Задает флаги привязки, используемые при выделении поверхностей Microsoft Direct3D 11 для образцов мультимедиа.
ms.assetid: C3B475B1-9A44-47EA-BCE7-D3D0FB56DDAC
title: Атрибут MF_SA_D3D11_BINDFLAGS (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb5ae4161a6782a3ea7a69b471044e43c5ee7a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345835"
---
# <a name="mf_sa_d3d11_bindflags-attribute"></a>\_Атрибут MF SA \_ D3D11 \_ биндфлагс

Задает флаги привязки, используемые при выделении поверхностей Microsoft Direct3D 11 для образцов мультимедиа.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Значение этого атрибута является побитовым **или** для флагов [**\_ \_ флага привязки D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) .

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                              |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
