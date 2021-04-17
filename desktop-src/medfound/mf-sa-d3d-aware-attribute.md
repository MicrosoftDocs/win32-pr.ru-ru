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
# <a name="mf_sa_d3d_aware-attribute"></a><span data-ttu-id="ce28c-104">\_Атрибут с \_ поддержкой D3D SA \_</span><span class="sxs-lookup"><span data-stu-id="ce28c-104">MF\_SA\_D3D\_AWARE attribute</span></span>

<span data-ttu-id="ce28c-105">Указывает, поддерживает ли преобразование Media Foundation (MFT) ускорение видео DirectX (ДКСВА).</span><span class="sxs-lookup"><span data-stu-id="ce28c-105">Specifies whether a Media Foundation transform (MFT) supports DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="ce28c-106">Этот атрибут применяется только к видео МФТС.</span><span class="sxs-lookup"><span data-stu-id="ce28c-106">This attribute applies only to video MFTs.</span></span>

## <a name="data-type"></a><span data-ttu-id="ce28c-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ce28c-107">Data type</span></span>

<span data-ttu-id="ce28c-108">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="ce28c-108">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ce28c-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce28c-109">Remarks</span></span>

<span data-ttu-id="ce28c-110">Чтобы запросить этот атрибут, вызовите [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) , чтобы получить глобальное хранилище атрибутов MFT.</span><span class="sxs-lookup"><span data-stu-id="ce28c-110">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span> <span data-ttu-id="ce28c-111">Если методы **InAttribute** выполнены, вызовите [**ИМФАТТРИБУТЕС:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="ce28c-111">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="ce28c-112">Этот атрибут сообщает клиенту, может ли MFT использовать видео Direct3D 9:</span><span class="sxs-lookup"><span data-stu-id="ce28c-112">This attribute tells the client whether the MFT can use Direct3D 9 video:</span></span>

-   <span data-ttu-id="ce28c-113">Если атрибут не равен нулю, клиент может предоставить MFT указатель на интерфейс [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) перед запуском потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="ce28c-113">If the attribute is nonzero, the client can give the MFT a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface before streaming starts.</span></span> <span data-ttu-id="ce28c-114">Для этого клиент отправляет в основную таблицу сообщений [**MFT \_ сообщение \_ \_ \_ диспетчера D3D**](mft-message-set-d3d-manager.md) .</span><span class="sxs-lookup"><span data-stu-id="ce28c-114">To do so, the client sends the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span> <span data-ttu-id="ce28c-115">Клиенту не требуется отсылать это сообщение.</span><span class="sxs-lookup"><span data-stu-id="ce28c-115">The client is not required to send this message.</span></span>
-   <span data-ttu-id="ce28c-116">Если этот атрибут равен нулю (**false**), то файл MFT не поддерживает видео Direct3D 9, и клиент не должен отсылать сообщение [**MFT \_ , \_ заданные \_ \_ диспетчером D3D**](mft-message-set-d3d-manager.md) в основную таблицу.</span><span class="sxs-lookup"><span data-stu-id="ce28c-116">If this attribute is zero (**FALSE**), the MFT does not support Direct3D 9 video, and the client should not send the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span>

<span data-ttu-id="ce28c-117">Значение этого атрибута по умолчанию равно **false**.</span><span class="sxs-lookup"><span data-stu-id="ce28c-117">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="ce28c-118">Рассматривайте этот атрибут как доступный только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ce28c-118">Treat this attribute as read-only.</span></span> <span data-ttu-id="ce28c-119">Не изменяйте значение. в MFT все изменения в значении будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="ce28c-119">Do not change the value; the MFT will ignore any changes to the value.</span></span>

<span data-ttu-id="ce28c-120">Дополнительные сведения о реализации этого атрибута в настраиваемой таблице MFT см. в разделе [МФТС с поддержкой Direct3D](direct3d-aware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="ce28c-120">For more information about implementing this attribute in a custom MFT, see [Direct3D-Aware MFTs](direct3d-aware-mfts.md).</span></span>

<span data-ttu-id="ce28c-121">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="ce28c-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="ce28c-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="ce28c-122">Examples</span></span>

<span data-ttu-id="ce28c-123">Следующий код проверяет, поддерживает ли MFT ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="ce28c-123">The following code tests whether an MFT supports DXVA.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ce28c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="ce28c-124">Requirements</span></span>



| <span data-ttu-id="ce28c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="ce28c-125">Requirement</span></span> | <span data-ttu-id="ce28c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ce28c-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce28c-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce28c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ce28c-128">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="ce28c-128">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="ce28c-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce28c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ce28c-130">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="ce28c-130">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ce28c-131">Header</span><span class="sxs-lookup"><span data-stu-id="ce28c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce28c-132"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce28c-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce28c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce28c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce28c-134">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ce28c-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ce28c-135">МФТС с поддержкой Direct3D</span><span class="sxs-lookup"><span data-stu-id="ce28c-135">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
</dt> <dt>

[<span data-ttu-id="ce28c-136">Поддержка ДКСВА 2,0 в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ce28c-136">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="ce28c-137">Преобразования Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ce28c-137">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="ce28c-138">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="ce28c-138">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="ce28c-139">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="ce28c-139">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ce28c-140">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ce28c-140">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ce28c-141">\_ \_ режим ДКСВА топологии \_ MF</span><span class="sxs-lookup"><span data-stu-id="ce28c-141">MF\_TOPOLOGY\_DXVA\_MODE</span></span>](mf-topology-dxva-mode.md)
</dt> </dl>

 

 




