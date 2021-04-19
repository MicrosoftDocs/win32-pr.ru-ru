---
description: Указывает сведения о документе, связанном с операцией DLP конечной точки.
title: Структура DLP_DOCUMENT_INFO (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_DOCUMENT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d588b627a4d5a88162cb0af67df1b5bf4fd943f1
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495960"
---
# <a name="dlp_document_info-structure"></a><span data-ttu-id="742e5-103">Структура DLP_DOCUMENT_INFO</span><span class="sxs-lookup"><span data-stu-id="742e5-103">DLP_DOCUMENT_INFO structure</span></span>

<span data-ttu-id="742e5-104">Указывает сведения о документе, связанном с операцией DLP конечной точки.</span><span class="sxs-lookup"><span data-stu-id="742e5-104">Specifies information about a document that is associated with an endpoint DLP operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="742e5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="742e5-105">Syntax</span></span>


```C++
typedef struct _DLP_DOCUMENT_INFO {

    DWORD Version;    
    LPCWSTR PersistentFileName;
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;
```


## <a name="members"></a><span data-ttu-id="742e5-106">Члены</span><span class="sxs-lookup"><span data-stu-id="742e5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="742e5-107">*Версия* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="742e5-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="742e5-108">Значение типа DWORD, указывающее версию API.</span><span class="sxs-lookup"><span data-stu-id="742e5-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="742e5-109">Это значение всегда должно быть **DLP_DOCUMENT_INFO_V_LATEST**.</span><span class="sxs-lookup"><span data-stu-id="742e5-109">This value should always be **DLP_DOCUMENT_INFO_V_LATEST**.</span></span> <span data-ttu-id="742e5-110">Эта константа определена в файле заголовка образца ендпоинтдлп. h, приведенном в статье [Защита от потери данных в конечной точке](endpointdlp-endpoint-data-loss-prevention.md)статьи.</span><span class="sxs-lookup"><span data-stu-id="742e5-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md).</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="742e5-111">*Персистентфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="742e5-111">*PersistentFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="742e5-112">Объект ЛПКВСТР, указывающий исходный путь к документу.</span><span class="sxs-lookup"><span data-stu-id="742e5-112">A LPCWSTR specifying the original path of the document.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="742e5-113">*Локалфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="742e5-113">*LocalFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="742e5-114">Объект ЛПКВСТР, указывающий путь к реальному резервному файлу документа.</span><span class="sxs-lookup"><span data-stu-id="742e5-114">A LPCWSTR specifying the path to the real backing file of the document.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="742e5-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="742e5-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="742e5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="742e5-116">Requirements</span></span>



| <span data-ttu-id="742e5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="742e5-117">Requirement</span></span>          |    <span data-ttu-id="742e5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="742e5-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="742e5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="742e5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="742e5-120">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="742e5-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

