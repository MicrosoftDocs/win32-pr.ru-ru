---
description: Функция-посредник для метода Commit.
ms.assetid: 5b3b90ad-9d67-4fbd-b01e-c7478df8dd45
title: Функция IWICFastMetadataEncoder_Commit_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFastMetadataEncoder_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 487fd99c68752b1547ba53c553025fc8ecfd5ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265301"
---
# <a name="iwicfastmetadataencoder_commit_proxy-function"></a><span data-ttu-id="72b82-103">Ивикфастметадатаенкодер \_ фиксация \_ прокси-функции</span><span class="sxs-lookup"><span data-stu-id="72b82-103">IWICFastMetadataEncoder\_Commit\_Proxy function</span></span>

<span data-ttu-id="72b82-104">Функция-посредник для метода [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-commit) .</span><span class="sxs-lookup"><span data-stu-id="72b82-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="72b82-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72b82-105">Syntax</span></span>


```C++
HRESULT IWICFastMetadataEncoder_Commit_Proxy(
  _In_ IWICFastMetadataEncoder *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="72b82-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="72b82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72b82-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="72b82-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72b82-108">Тип: \**[**ивикфастметадатаенкодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="72b82-108">Type: \**[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\** _</span></span>

<span data-ttu-id="72b82-109">Указатель на этот объект [_ *ивикфастметадатаенкодер* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) .</span><span class="sxs-lookup"><span data-stu-id="72b82-109">Pointer to this [_ *IWICFastMetadataEncoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72b82-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="72b82-110">Return value</span></span>

<span data-ttu-id="72b82-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="72b82-111">Type: **HRESULT**</span></span>

<span data-ttu-id="72b82-112">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="72b82-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="72b82-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="72b82-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="72b82-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="72b82-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="72b82-115">Требования</span><span class="sxs-lookup"><span data-stu-id="72b82-115">Requirements</span></span>



| <span data-ttu-id="72b82-116">Требование</span><span class="sxs-lookup"><span data-stu-id="72b82-116">Requirement</span></span> | <span data-ttu-id="72b82-117">Значение</span><span class="sxs-lookup"><span data-stu-id="72b82-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72b82-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="72b82-118">Minimum supported client</span></span><br/> | <span data-ttu-id="72b82-119">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="72b82-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="72b82-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="72b82-120">Minimum supported server</span></span><br/> | <span data-ttu-id="72b82-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="72b82-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="72b82-122">DLL</span><span class="sxs-lookup"><span data-stu-id="72b82-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72b82-123"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72b82-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




