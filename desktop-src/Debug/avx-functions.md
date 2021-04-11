---
description: Функции Intel AVX.
ms.assetid: 237f356a-9ee8-4c52-b08c-a6695c52713a
title: Функции AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0b56c83b6beb674bc284b139bb656441956705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262502"
---
# <a name="avx-functions"></a><span data-ttu-id="10b63-103">Функции AVX</span><span class="sxs-lookup"><span data-stu-id="10b63-103">AVX Functions</span></span>

<span data-ttu-id="10b63-104">Ниже перечислены функции Intel AVX.</span><span class="sxs-lookup"><span data-stu-id="10b63-104">The following are the Intel AVX functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="10b63-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="10b63-105">In this section</span></span>



| <span data-ttu-id="10b63-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="10b63-106">Topic</span></span>                                                                   | <span data-ttu-id="10b63-107">Описание</span><span class="sxs-lookup"><span data-stu-id="10b63-107">Description</span></span>                                                                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10b63-108">**копиконтекст**</span><span class="sxs-lookup"><span data-stu-id="10b63-108">**CopyContext**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copycontext)<br/>                           | <span data-ttu-id="10b63-109">Копирует исходную структуру контекста (включая любые Ксстате) в инициализированную структуру контекста назначения.</span><span class="sxs-lookup"><span data-stu-id="10b63-109">Copies a source context structure (including any XState) onto an initialized destination context structure.</span></span><br/>         |
| [<span data-ttu-id="10b63-110">**жетенабледксстатефеатурес**</span><span class="sxs-lookup"><span data-stu-id="10b63-110">**GetEnabledXStateFeatures**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getenabledxstatefeatures)<br/> | <span data-ttu-id="10b63-111">Возвращает маску включенных функций Ксстате на процессорах x86 или x64.</span><span class="sxs-lookup"><span data-stu-id="10b63-111">Gets a mask of enabled XState features on x86 or x64 processors.</span></span><br/>                                                    |
| [<span data-ttu-id="10b63-112">**жетксстатефеатуресмаск**</span><span class="sxs-lookup"><span data-stu-id="10b63-112">**GetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)<br/>       | <span data-ttu-id="10b63-113">Возвращает маску функций Ксстате, установленных в структуре [**контекста**](/windows/desktop/api/WinNT/ns-winnt-wow64_context) .</span><span class="sxs-lookup"><span data-stu-id="10b63-113">Returns the mask of XState features set within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-wow64_context) structure.</span></span><br/>                        |
| [<span data-ttu-id="10b63-114">**инитиализеконтекст**</span><span class="sxs-lookup"><span data-stu-id="10b63-114">**InitializeContext**</span></span>](/windows/desktop/api/WinBase/nf-winbase-initializecontext)<br/>               | <span data-ttu-id="10b63-115">Инициализирует структуру [**контекста**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) в буфере с требуемым размером и выравниванием.</span><span class="sxs-lookup"><span data-stu-id="10b63-115">Initializes a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure inside a buffer with the necessary size and alignment.</span></span><br/>       |
| [<span data-ttu-id="10b63-116">**локатексстатефеатуре**</span><span class="sxs-lookup"><span data-stu-id="10b63-116">**LocateXStateFeature**</span></span>](/windows/desktop/api/WinBase/nf-winbase-locatexstatefeature)<br/>           | <span data-ttu-id="10b63-117">Получает указатель на состояние процессора для функции Ксстате в структуре [**контекста**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) .</span><span class="sxs-lookup"><span data-stu-id="10b63-117">Retrieves a pointer to the processor state for an XState feature within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure.</span></span><br/> |
| [<span data-ttu-id="10b63-118">**сетксстатефеатуресмаск**</span><span class="sxs-lookup"><span data-stu-id="10b63-118">**SetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setxstatefeaturesmask)<br/>       | <span data-ttu-id="10b63-119">Задает маску функций Ксстате, установленных в структуре [**контекста**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) .</span><span class="sxs-lookup"><span data-stu-id="10b63-119">Sets the mask of XState features set within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure.</span></span><br/>                             |



 

 

 




