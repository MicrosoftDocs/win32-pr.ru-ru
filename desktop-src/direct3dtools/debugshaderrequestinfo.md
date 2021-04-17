---
description: Представляет сведения о запросе отладчика шейдеров.
MS-HAID: vspixengine.DebugShaderRequestInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Дебугшадеррекуестинфо
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DEFFAEE4-6C53-4C89-A533-A5BE73B80DEA
api_name:
- DebugShaderRequestInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a59bfb84bb7d4e8644c0cfadc4475be7d7da4a54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537343"
---
# <a name="span-idvspixenginedebugshaderrequestinfospandebugshaderrequestinfo-structure"></a><span data-ttu-id="f74e1-103"><span id="vspixengine.debugshaderrequestinfo"></span>Структура Дебугшадеррекуестинфо</span><span class="sxs-lookup"><span data-stu-id="f74e1-103"><span id="vspixengine.debugshaderrequestinfo"></span>DebugShaderRequestInfo structure</span></span>

<span data-ttu-id="f74e1-104">Представляет сведения о запросе отладчика шейдеров.</span><span class="sxs-lookup"><span data-stu-id="f74e1-104">Represents information about a shader debugger request.</span></span>

## <a name="syntax"></a><span data-ttu-id="f74e1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f74e1-105">Syntax</span></span>


```C++
} DebugShaderRequestInfo;
```

## <a name="members"></a><span data-ttu-id="f74e1-106">Члены</span><span class="sxs-lookup"><span data-stu-id="f74e1-106">Members</span></span>

<span data-ttu-id="f74e1-107">**Backstage**</span><span class="sxs-lookup"><span data-stu-id="f74e1-107">**stage**</span></span>  
<span data-ttu-id="f74e1-108">Стадия конвейера для отладки.</span><span class="sxs-lookup"><span data-stu-id="f74e1-108">The pipeline stage to debug.</span></span>

<span data-ttu-id="f74e1-109">**1008**</span><span class="sxs-lookup"><span data-stu-id="f74e1-109">**eventID**</span></span>  
<span data-ttu-id="f74e1-110">Идентификатор события графики для отладки.</span><span class="sxs-lookup"><span data-stu-id="f74e1-110">The ID of the graphics event to debug.</span></span>

<span data-ttu-id="f74e1-111">**фраменумбер**</span><span class="sxs-lookup"><span data-stu-id="f74e1-111">**frameNumber**</span></span>  
<span data-ttu-id="f74e1-112">Кадр для отладки.</span><span class="sxs-lookup"><span data-stu-id="f74e1-112">The frame to debug.</span></span>

<span data-ttu-id="f74e1-113">**положений**</span><span class="sxs-lookup"><span data-stu-id="f74e1-113">**vertex**</span></span>  
<span data-ttu-id="f74e1-114">Вершина для отладки.</span><span class="sxs-lookup"><span data-stu-id="f74e1-114">The vertex to debug.</span></span>

<span data-ttu-id="f74e1-115">**растров**</span><span class="sxs-lookup"><span data-stu-id="f74e1-115">**pixel**</span></span>  
<span data-ttu-id="f74e1-116">Пиксель для отладки.</span><span class="sxs-lookup"><span data-stu-id="f74e1-116">The pixel to debug.</span></span>

<span data-ttu-id="f74e1-117">**граупкурдинатес**</span><span class="sxs-lookup"><span data-stu-id="f74e1-117">**groupCoordinates**</span></span>  
<span data-ttu-id="f74e1-118">Координаты группы для отладки.</span><span class="sxs-lookup"><span data-stu-id="f74e1-118">The coordinates of the group to debug.</span></span>

<span data-ttu-id="f74e1-119">**среадкурдинатес**</span><span class="sxs-lookup"><span data-stu-id="f74e1-119">**threadCoordinates**</span></span>  
<span data-ttu-id="f74e1-120">Координаты отлаживаемого потока</span><span class="sxs-lookup"><span data-stu-id="f74e1-120">The coordinates of the thread to debug</span></span>

## <a name="requirements"></a><span data-ttu-id="f74e1-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f74e1-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f74e1-122">Header</span><span class="sxs-lookup"><span data-stu-id="f74e1-122">Header</span></span></p></td><td><span data-ttu-id="f74e1-123">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="f74e1-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



