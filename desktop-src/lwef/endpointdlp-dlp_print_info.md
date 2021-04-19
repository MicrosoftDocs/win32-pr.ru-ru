---
description: Указывает сведения о документе, связанном с операцией печати в конечной точке.
title: Структура DLP_PRINT_INFO (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_PRINT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 37bde9f62de07083aac6a3d2fb367b021caf3732
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495959"
---
# <a name="dlp_print_info-structure"></a><span data-ttu-id="713c1-103">Структура DLP_PRINT_INFO</span><span class="sxs-lookup"><span data-stu-id="713c1-103">DLP_PRINT_INFO structure</span></span>

<span data-ttu-id="713c1-104">Указывает сведения о документе, связанном с операцией печати в конечной точке.</span><span class="sxs-lookup"><span data-stu-id="713c1-104">Specifies information about a document that is associated with an endpoint DLP print operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="713c1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="713c1-105">Syntax</span></span>


```C++
typedef struct _DLP_PRINT_INFO {
    DWORD Version;
    LPCWSTR PrinterName;
    LPCWSTR JobName;
    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;
```


## <a name="members"></a><span data-ttu-id="713c1-106">Члены</span><span class="sxs-lookup"><span data-stu-id="713c1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="713c1-107">*Версия* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="713c1-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="713c1-108">Значение типа DWORD, указывающее версию API.</span><span class="sxs-lookup"><span data-stu-id="713c1-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="713c1-109">Это значение всегда должно быть **DLP_PRINT_INFO_V_LATEST**.</span><span class="sxs-lookup"><span data-stu-id="713c1-109">This value should always be **DLP_PRINT_INFO_V_LATEST**.</span></span> <span data-ttu-id="713c1-110">Эта константа определена в файле заголовка образца ендпоинтдлп. h, приведенном в статье [Защита от потери данных в конечной точке](endpointdlp-endpoint-data-loss-prevention.md)статьи.</span><span class="sxs-lookup"><span data-stu-id="713c1-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md).</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="713c1-111">*Принтернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="713c1-111">*PrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="713c1-112">ЛПКВСТР, определяющий принтер назначения.</span><span class="sxs-lookup"><span data-stu-id="713c1-112">A LPCWSTR identifying the destination printer.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="713c1-113">*JobName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="713c1-113">*JobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="713c1-114">ЛПКВСТР, указывающий имя задания печати.</span><span class="sxs-lookup"><span data-stu-id="713c1-114">A LPCWSTR specifying print job name.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="713c1-115">*OutputFilename* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="713c1-115">*OutputFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="713c1-116">Объект ЛПКВСТР, указывающий путь к выходному файлу при печати в файл.</span><span class="sxs-lookup"><span data-stu-id="713c1-116">A LPCWSTR specifying the path to the output file, when printing to a file.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="713c1-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="713c1-117">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="713c1-118">Требования</span><span class="sxs-lookup"><span data-stu-id="713c1-118">Requirements</span></span>



| <span data-ttu-id="713c1-119">Требование</span><span class="sxs-lookup"><span data-stu-id="713c1-119">Requirement</span></span>          |    <span data-ttu-id="713c1-120">Значение</span><span class="sxs-lookup"><span data-stu-id="713c1-120">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="713c1-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="713c1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="713c1-122">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="713c1-122">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

