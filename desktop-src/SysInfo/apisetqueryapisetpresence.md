---
description: Этот API предназначен только для внутреннего использования и не должен использоваться в коде.
ms.assetid: 836A7515-8C22-4032-9E99-F89B32C21685
title: Функция Аписеткуеряписетпресенце (Apiquery. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApiSetQueryApiSetPresence
api_type:
- DllExport
api_location:
- api-ms-win-core-apiquery-l1-1-0.dll
- ntdll.dll
ms.openlocfilehash: 738a69b0d08f7e619dbd64229d0c13b2ae7dfaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664720"
---
# <a name="apisetqueryapisetpresence-function"></a><span data-ttu-id="be230-103">Функция Аписеткуеряписетпресенце</span><span class="sxs-lookup"><span data-stu-id="be230-103">ApiSetQueryApiSetPresence function</span></span>

<span data-ttu-id="be230-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="be230-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="be230-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="be230-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="be230-106">Этот API предназначен только для внутреннего использования и не должен использоваться в коде.</span><span class="sxs-lookup"><span data-stu-id="be230-106">This API is intended for internal use only and should not be used in your code.</span></span>

## <a name="syntax"></a><span data-ttu-id="be230-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be230-107">Syntax</span></span>


```C++
BOOL WINAPI ApiSetQueryApiSetPresence(
  _In_  PCUNICODE_STRING Namespace,
  _Out_ PBOOLEAN         Present
);
```



## <a name="parameters"></a><span data-ttu-id="be230-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="be230-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be230-109">*Пространство имен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be230-109">*Namespace* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="be230-110">*Имеется* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="be230-110">*Present* \[out\]</span></span>
<span data-ttu-id="be230-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="be230-111"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="be230-112">Требования</span><span class="sxs-lookup"><span data-stu-id="be230-112">Requirements</span></span>



| <span data-ttu-id="be230-113">Требование</span><span class="sxs-lookup"><span data-stu-id="be230-113">Requirement</span></span> | <span data-ttu-id="be230-114">Значение</span><span class="sxs-lookup"><span data-stu-id="be230-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be230-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be230-115">Minimum supported client</span></span><br/> | <span data-ttu-id="be230-116">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="be230-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                                                           |
| <span data-ttu-id="be230-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be230-117">Minimum supported server</span></span><br/> | <span data-ttu-id="be230-118">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="be230-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="be230-119">Header</span><span class="sxs-lookup"><span data-stu-id="be230-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="be230-120"><dt>Apiquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="be230-120"><dt>Apiquery.h</dt></span></span> </dl>                                                                                                                 |
| <span data-ttu-id="be230-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="be230-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="be230-122"><dt>API-MS-Win-Core-apiquery-L1. lib; </dt> <dt>API-MS-Win-Core-apiquery-L1-1 -0. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be230-122"><dt>Api-ms-win-core-apiquery-l1.lib; </dt> <dt>Api-ms-win-core-apiquery-l1-1-0.lib</dt></span></span> </dl> |
| <span data-ttu-id="be230-123">DLL</span><span class="sxs-lookup"><span data-stu-id="be230-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be230-124"><dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be230-124"><dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt></span></span> </dl>                                                                                        |



 

 




