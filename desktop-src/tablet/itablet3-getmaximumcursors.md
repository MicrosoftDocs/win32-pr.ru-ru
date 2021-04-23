---
description: Метод Жетмаксимумкурсорс извлекает максимальное число курсоров, поддерживаемое планшетным устройством.
ms.assetid: 5a43d792-e64c-4506-9792-31efe0885959
title: 'Метод ITablet3:: Жетмаксимумкурсорс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.GetMaximumCursors
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7c40184d35ac1d42cb5f5e845396b40efc2d928e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719562"
---
# <a name="itablet3getmaximumcursors-method"></a><span data-ttu-id="0d65a-103">Метод ITablet3:: Жетмаксимумкурсорс</span><span class="sxs-lookup"><span data-stu-id="0d65a-103">ITablet3::GetMaximumCursors method</span></span>

<span data-ttu-id="0d65a-104">Метод **жетмаксимумкурсорс** извлекает максимальное число курсоров, поддерживаемое планшетным устройством.</span><span class="sxs-lookup"><span data-stu-id="0d65a-104">The **GetMaximumCursors** method retrieves the maximum number of cursors that a tablet device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d65a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d65a-105">Syntax</span></span>


```C++
HRESULT GetMaximumCursors(
   ULONG *pMaximumCursors
);
```



## <a name="parameters"></a><span data-ttu-id="0d65a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d65a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d65a-107">*пмаксимумкурсорс*</span><span class="sxs-lookup"><span data-stu-id="0d65a-107">*pMaximumCursors*</span></span> 
</dt> <dd>

<span data-ttu-id="0d65a-108">Максимальное число входов, поддерживаемое устройством.</span><span class="sxs-lookup"><span data-stu-id="0d65a-108">The maximum number of inputs that the device supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d65a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d65a-109">Return value</span></span>

<span data-ttu-id="0d65a-110">Возвращает значение S \_ ОК в случае успеха; в противном случае возвращает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="0d65a-110">Returns S\_OK on success; otherwise, returns an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d65a-111">Требования</span><span class="sxs-lookup"><span data-stu-id="0d65a-111">Requirements</span></span>



| <span data-ttu-id="0d65a-112">Требование</span><span class="sxs-lookup"><span data-stu-id="0d65a-112">Requirement</span></span> | <span data-ttu-id="0d65a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0d65a-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d65a-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d65a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0d65a-115">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0d65a-115">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0d65a-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d65a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0d65a-117">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d65a-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0d65a-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0d65a-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="0d65a-119"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0d65a-119"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d65a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d65a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d65a-121">**ITablet3**</span><span class="sxs-lookup"><span data-stu-id="0d65a-121">**ITablet3**</span></span>](itablet3.md)
</dt> </dl>

 

 




