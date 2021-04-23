---
description: Не реализован.
ms.assetid: d0fc571f-79f5-448a-8082-6e5f7f48118f
title: 'Метод IXml2Dex:: Вритексмлпарт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8f194fe409d8ea94f786fe3802b2c758a1a00520
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673069"
---
# <a name="ixml2dexwritexmlpart-method"></a><span data-ttu-id="43c61-103">Метод IXml2Dex:: Вритексмлпарт</span><span class="sxs-lookup"><span data-stu-id="43c61-103">IXml2Dex::WriteXMLPart method</span></span>

> [!Note]  
> <span data-ttu-id="43c61-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="43c61-104">\[Deprecated.</span></span> <span data-ttu-id="43c61-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="43c61-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="43c61-106">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="43c61-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="43c61-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43c61-107">Syntax</span></span>


```C++
HRESULT WriteXMLPart(
   IUnknown *pTimeline,
   double   dStart,
   double   dEnd,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="43c61-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="43c61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43c61-109">*птимелине*</span><span class="sxs-lookup"><span data-stu-id="43c61-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="43c61-110">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="43c61-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="43c61-111">*дстарт*</span><span class="sxs-lookup"><span data-stu-id="43c61-111">*dStart*</span></span> 
</dt> <dd>

<span data-ttu-id="43c61-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="43c61-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="43c61-113">*денд*</span><span class="sxs-lookup"><span data-stu-id="43c61-113">*dEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="43c61-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="43c61-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="43c61-115">*FileName*</span><span class="sxs-lookup"><span data-stu-id="43c61-115">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="43c61-116">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="43c61-116">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43c61-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43c61-117">Return value</span></span>

<span data-ttu-id="43c61-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="43c61-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="43c61-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="43c61-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="43c61-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43c61-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="43c61-121">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="43c61-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="43c61-122">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="43c61-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="43c61-123">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="43c61-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="43c61-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43c61-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43c61-125">**Интерфейс IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="43c61-125">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> </dl>

 

 



