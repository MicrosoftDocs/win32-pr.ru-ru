---
description: Возвращает объект ключей мультимедиа, связанный с обработчиком мультимедиа, или значение null, если отсутствует объект ключей мультимедиа.
ms.assetid: e6556a02-445d-4436-80de-e4156d6a3d63
title: 'Метод Имфмедиаенгиниме:: get_Keys'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineEME.get_Keys
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: dcb06352065b28739a616a9f2216c20eedebb913
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713296"
---
# <a name="imfmediaengineemeget_keys-method"></a><span data-ttu-id="f94af-103">Метод Имфмедиаенгиниме:: Get \_ Keys</span><span class="sxs-lookup"><span data-stu-id="f94af-103">IMFMediaEngineEME::get\_Keys method</span></span>

<span data-ttu-id="f94af-104">Возвращает объект ключей мультимедиа, связанный с обработчиком мультимедиа, или **значение NULL** , если отсутствует объект ключей мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f94af-104">Gets the media keys object associated with the media engine or **null** if there is not a media keys object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f94af-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f94af-105">Syntax</span></span>


```C++
HRESULT get_Keys(
   IMFMediaKeys **keys
);
```



## <a name="parameters"></a><span data-ttu-id="f94af-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f94af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f94af-107">*ключ*</span><span class="sxs-lookup"><span data-stu-id="f94af-107">*keys*</span></span> 
</dt> <dd>

<span data-ttu-id="f94af-108">Объект ключей мультимедиа, связанный с обработчиком мультимедиа, или **значение NULL** , если отсутствует объект ключей мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f94af-108">The media keys object associated with the media engine or **null** if there is not a media keys object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f94af-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f94af-109">Return value</span></span>

<span data-ttu-id="f94af-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f94af-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f94af-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f94af-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f94af-112">Требования</span><span class="sxs-lookup"><span data-stu-id="f94af-112">Requirements</span></span>



| <span data-ttu-id="f94af-113">Требование</span><span class="sxs-lookup"><span data-stu-id="f94af-113">Requirement</span></span> | <span data-ttu-id="f94af-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f94af-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f94af-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f94af-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f94af-116">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f94af-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f94af-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f94af-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f94af-118">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f94af-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f94af-119">IDL</span><span class="sxs-lookup"><span data-stu-id="f94af-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f94af-120"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f94af-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f94af-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f94af-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f94af-122">**имфмедиаенгиниме**</span><span class="sxs-lookup"><span data-stu-id="f94af-122">**IMFMediaEngineEME**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme)
</dt> </dl>

 

 




