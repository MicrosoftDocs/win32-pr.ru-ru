---
description: 'Дополнительные сведения о методе: Имфмедиакэйс:: Shutdown'
ms.assetid: 464b598c-5fa7-40af-83ba-8619fbd84b04
title: 'Метод Имфмедиакэйс:: Shutdown'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.Shutdown
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9fcee861b53aaf0c9fda2c6265f50fcee60f674c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351565"
---
# <a name="imfmediakeysshutdown-method"></a><span data-ttu-id="d563d-103">Метод Имфмедиакэйс:: Shutdown</span><span class="sxs-lookup"><span data-stu-id="d563d-103">IMFMediaKeys::Shutdown method</span></span>

## <a name="syntax"></a><span data-ttu-id="d563d-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d563d-104">Syntax</span></span>


```C++
HRESULT Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="d563d-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="d563d-105">Parameters</span></span>

<span data-ttu-id="d563d-106">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d563d-106">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d563d-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d563d-107">Return value</span></span>

<span data-ttu-id="d563d-108">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d563d-108">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d563d-109">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d563d-109">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d563d-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d563d-110">Remarks</span></span>

<span data-ttu-id="d563d-111">Перед окончательным выпуском должно быть вызвано **Завершение работы** приложения.</span><span class="sxs-lookup"><span data-stu-id="d563d-111">**Shutdown** should be called by the application before final release.</span></span> <span data-ttu-id="d563d-112">В этой точке выпускается ссылка на модуль расшифровки содержимого (CDM) и другие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="d563d-112">The Content Decryption Module (CDM) reference and any other resources is released at this point.</span></span> <span data-ttu-id="d563d-113">Однако связанные сеансы не освобождаются или не закрываются.</span><span class="sxs-lookup"><span data-stu-id="d563d-113">However, related sessions are not freed or closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d563d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d563d-114">Requirements</span></span>



| <span data-ttu-id="d563d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d563d-115">Requirement</span></span> | <span data-ttu-id="d563d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d563d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d563d-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d563d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d563d-118">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d563d-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d563d-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d563d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d563d-120">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d563d-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d563d-121">IDL</span><span class="sxs-lookup"><span data-stu-id="d563d-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d563d-122"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d563d-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d563d-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d563d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d563d-124">**имфмедиакэйс**</span><span class="sxs-lookup"><span data-stu-id="d563d-124">**IMFMediaKeys**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




