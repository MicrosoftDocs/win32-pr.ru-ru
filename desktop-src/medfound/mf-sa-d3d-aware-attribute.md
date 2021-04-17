---
description: Указывает, поддерживает ли преобразование Media Foundation (MFT) ускорение видео DirectX (ДКСВА). Этот атрибут применяется только к видео МФТС.
ms.assetid: db6a8b20-fda0-4ffe-b1b5-a77b7604d290
title: Атрибут MF_SA_D3D_AWARE (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb0de8c5a66eaa89f66becf6770f69e6449c1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702549"
---
# <a name="mf_sa_d3d_aware-attribute"></a>\_Атрибут с \_ поддержкой D3D SA \_

Указывает, поддерживает ли преобразование Media Foundation (MFT) ускорение видео DirectX (ДКСВА). Этот атрибут применяется только к видео МФТС.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="remarks"></a>Комментарии

Чтобы запросить этот атрибут, вызовите [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) , чтобы получить глобальное хранилище атрибутов MFT. Если методы **InAttribute** выполнены, вызовите [**ИМФАТТРИБУТЕС:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Этот атрибут сообщает клиенту, может ли MFT использовать видео Direct3D 9:

-   Если атрибут не равен нулю, клиент может предоставить MFT указатель на интерфейс [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) перед запуском потоковой передачи. Для этого клиент отправляет в основную таблицу сообщений [**MFT \_ сообщение \_ \_ \_ диспетчера D3D**](mft-message-set-d3d-manager.md) . Клиенту не требуется отсылать это сообщение.
-   Если этот атрибут равен нулю (**false**), то файл MFT не поддерживает видео Direct3D 9, и клиент не должен отсылать сообщение [**MFT \_ , \_ заданные \_ \_ диспетчером D3D**](mft-message-set-d3d-manager.md) в основную таблицу.

Значение этого атрибута по умолчанию равно **false**. Рассматривайте этот атрибут как доступный только для чтения. Не изменяйте значение. в MFT все изменения в значении будут игнорироваться.

Дополнительные сведения о реализации этого атрибута в настраиваемой таблице MFT см. в разделе [МФТС с поддержкой Direct3D](direct3d-aware-mfts.md).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="examples"></a>Примеры

Следующий код проверяет, поддерживает ли MFT ДКСВА.


```C++
// Returns TRUE is an MFT supports DirectX Video Acceleration.

BOOL IsTransformD3DAware(IMFTransform *pMFT)
{
    BOOL bD3DAware = FALSE;
    
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bD3DAware = MFGetAttributeUINT32(pAttributes, MF_SA_D3D_AWARE, FALSE);
        pAttributes->Release();
    }
    return bD3DAware;
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>                                    |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/>                              |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[МФТС с поддержкой Direct3D](direct3d-aware-mfts.md)
</dt> <dt>

[Поддержка ДКСВА 2,0 в Media Foundation](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[Преобразования Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[\_ \_ режим ДКСВА топологии \_ MF](mf-topology-dxva-mode.md)
</dt> </dl>

 

 




