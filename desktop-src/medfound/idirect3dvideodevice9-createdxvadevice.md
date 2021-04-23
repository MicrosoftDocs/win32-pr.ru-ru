---
description: Создает устройство декодера DirectX Video Acceleration (ДКСВА).
ms.assetid: aeebf65f-1bde-4a33-87cd-25c62dcc0248
title: 'Метод IDirect3DVideoDevice9:: Креатедксвадевице (Дксва. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateDXVADevice
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 50ce7cee350479f4286921b6cdf69b319033c721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155187"
---
# <a name="idirect3dvideodevice9createdxvadevice-method"></a><span data-ttu-id="a672a-103">Метод IDirect3DVideoDevice9:: Креатедксвадевице</span><span class="sxs-lookup"><span data-stu-id="a672a-103">IDirect3DVideoDevice9::CreateDXVADevice method</span></span>

<span data-ttu-id="a672a-104">Создает устройство декодера DirectX Video Acceleration (ДКСВА).</span><span class="sxs-lookup"><span data-stu-id="a672a-104">Creates a DirectX Video Acceleration (DXVA) decoder device.</span></span>

## <a name="syntax"></a><span data-ttu-id="a672a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a672a-105">Syntax</span></span>


```C++
HRESULT CreateDXVADevice(
   GUID                 *pGuid,
   DXVAUncompDataInfo   *pUncompData,
   LPVOID               pData,
   DWORD                DataSize,
   IDirect3DDXVADevice9 **ppDXVADevice
);
```



## <a name="parameters"></a><span data-ttu-id="a672a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a672a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a672a-107">*пгуид*</span><span class="sxs-lookup"><span data-stu-id="a672a-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="a672a-108">Указатель на идентификатор GUID, указывающий создаваемое устройство.</span><span class="sxs-lookup"><span data-stu-id="a672a-108">Pointer to a GUID that specifies the device to create.</span></span>

</dd> <dt>

<span data-ttu-id="a672a-109">*пункомпдата*</span><span class="sxs-lookup"><span data-stu-id="a672a-109">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="a672a-110">Указатель на структуру [**дксваункомпдатаинфо**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) , которая задает формат несжатого изображения.</span><span class="sxs-lookup"><span data-stu-id="a672a-110">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the format of the uncompressed image.</span></span>

</dd> <dt>

<span data-ttu-id="a672a-111">*pData*</span><span class="sxs-lookup"><span data-stu-id="a672a-111">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="a672a-112">Указатель на структуру **\_ коннектмоде дксва** , которая указывает режим дксва и ограниченный профиль.</span><span class="sxs-lookup"><span data-stu-id="a672a-112">Pointer to a **DXVA\_ConnectMode** structure that specifies the DXVA mode and restricted profile.</span></span>

</dd> <dt>

<span data-ttu-id="a672a-113">*DataSize*</span><span class="sxs-lookup"><span data-stu-id="a672a-113">*DataSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a672a-114">Размер структуры **\_ коннектмоде дксва** в байтах.</span><span class="sxs-lookup"><span data-stu-id="a672a-114">Size of the **DXVA\_ConnectMode** structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a672a-115">*ппдксвадевице*</span><span class="sxs-lookup"><span data-stu-id="a672a-115">*ppDXVADevice*</span></span> 
</dt> <dd>

<span data-ttu-id="a672a-116">Получает указатель на интерфейс [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) .</span><span class="sxs-lookup"><span data-stu-id="a672a-116">Receives a pointer to the [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) interface.</span></span> <span data-ttu-id="a672a-117">Вызывающий объект должен освободить интерфейс.</span><span class="sxs-lookup"><span data-stu-id="a672a-117">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a672a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a672a-118">Return value</span></span>

<span data-ttu-id="a672a-119">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a672a-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a672a-120">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a672a-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a672a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a672a-121">Requirements</span></span>



| <span data-ttu-id="a672a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a672a-122">Requirement</span></span> | <span data-ttu-id="a672a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a672a-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a672a-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a672a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a672a-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a672a-125">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a672a-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a672a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a672a-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a672a-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a672a-128">Header</span><span class="sxs-lookup"><span data-stu-id="a672a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a672a-129"><dt>Дксва. h</dt></span><span class="sxs-lookup"><span data-stu-id="a672a-129"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a672a-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a672a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a672a-131">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="a672a-131">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




