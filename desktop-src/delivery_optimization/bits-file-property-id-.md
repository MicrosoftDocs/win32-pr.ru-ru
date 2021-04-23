---
title: Перечисление BITS_FILE_PROPERTY_ID (Deliveryoptimization. h)
description: В перечислении BITS_FILE_PROPERTY_ID указываются значения, определяющие значения ИДЕНТИФИКАТОРов, соответствующие свойствам Баккграундкопифиле.
ms.assetid: 47EFD160-7CA8-48E6-A18E-38D85F7C6E47
keywords:
- Перечисление BITS_FILE_PROPERTY_ID
- Перечисление BITS_FILE_PROPERTY_ID
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_ID
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b6c6b8a4de359e8313e3127080f2cc17ae6478c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710476"
---
# <a name="bits_file_property_id-enumeration"></a><span data-ttu-id="24e27-105">Перечисление BITS_FILE_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="24e27-105">BITS_FILE_PROPERTY_ID enumeration</span></span>

<span data-ttu-id="24e27-106">В перечислении **BITS_FILE_PROPERTY_ID** указываются значения, определяющие значения идентификаторов, соответствующие свойствам **баккграундкопифиле** .</span><span class="sxs-lookup"><span data-stu-id="24e27-106">The **BITS_FILE_PROPERTY_ID** enumeration specifies values that define ID values corresponding to **BackgroundCopyFile** properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="24e27-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24e27-107">Syntax</span></span>


```C++
typedef enum _BITS_FILE_PROPERTY_ID { 
  BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS  = 1
} BITS_FILE_PROPERTY_ID;
```



## <a name="constants"></a><span data-ttu-id="24e27-108">Константы</span><span class="sxs-lookup"><span data-stu-id="24e27-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="24e27-109"><span id="BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS"></span><span id="bits_file_property_id_http_response_headers"></span>**BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**</span><span class="sxs-lookup"><span data-stu-id="24e27-109"><span id="BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS"></span><span id="bits_file_property_id_http_response_headers"></span>**BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**</span></span>
</dt> <dd>

<span data-ttu-id="24e27-110">Полный набор HTTP-заголовков ответа из последнего HTTP-пакета ответа сервера.</span><span class="sxs-lookup"><span data-stu-id="24e27-110">The full set of HTTP response headers from the server's last HTTP response packet.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24e27-111">Требования</span><span class="sxs-lookup"><span data-stu-id="24e27-111">Requirements</span></span>



| <span data-ttu-id="24e27-112">Требование</span><span class="sxs-lookup"><span data-stu-id="24e27-112">Requirement</span></span> | <span data-ttu-id="24e27-113">Значение</span><span class="sxs-lookup"><span data-stu-id="24e27-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24e27-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24e27-114">Minimum supported client</span></span><br/> | <span data-ttu-id="24e27-115">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="24e27-115">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="24e27-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24e27-116">Minimum supported server</span></span><br/> | <span data-ttu-id="24e27-117">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="24e27-117">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="24e27-118">Header</span><span class="sxs-lookup"><span data-stu-id="24e27-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="24e27-119"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="24e27-119"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





