---
description: Представляет тип пути, используемого в качестве аргумента.
ms.assetid: f308c638-b383-432e-9dd3-edc33b792139
title: Перечисление PATH_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATH_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1e5602aa7384c8de6c33b407e9a536141d8d002b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538366"
---
# <a name="path_type-enumeration"></a><span data-ttu-id="0ba23-103">\_Перечисление типов путей</span><span class="sxs-lookup"><span data-stu-id="0ba23-103">PATH\_TYPE enumeration</span></span>

<span data-ttu-id="0ba23-104">Представляет тип пути, используемого в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="0ba23-104">Represents the type of path being used as an argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ba23-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ba23-105">Syntax</span></span>


```C++
typedef enum _PATH_TYPE { 
  DOS_PATH,
  NT_PATH
} PATH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="0ba23-106">Константы</span><span class="sxs-lookup"><span data-stu-id="0ba23-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0ba23-107"><span id="DOS_PATH"></span><span id="dos_path"></span>**\_путь к DOS**</span><span class="sxs-lookup"><span data-stu-id="0ba23-107"><span id="DOS_PATH"></span><span id="dos_path"></span>**DOS\_PATH**</span></span>
</dt> <dd>

<span data-ttu-id="0ba23-108">Стандартный путь.</span><span class="sxs-lookup"><span data-stu-id="0ba23-108">Standard path.</span></span>

</dd> <dt>

<span data-ttu-id="0ba23-109"><span id="NT_PATH"></span><span id="nt_path"></span>**\_путь NT**</span><span class="sxs-lookup"><span data-stu-id="0ba23-109"><span id="NT_PATH"></span><span id="nt_path"></span>**NT\_PATH**</span></span>
</dt> <dd>

<span data-ttu-id="0ba23-110">Внутренний путь.</span><span class="sxs-lookup"><span data-stu-id="0ba23-110">Internal path.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ba23-111">Требования</span><span class="sxs-lookup"><span data-stu-id="0ba23-111">Requirements</span></span>



| <span data-ttu-id="0ba23-112">Требование</span><span class="sxs-lookup"><span data-stu-id="0ba23-112">Requirement</span></span> | <span data-ttu-id="0ba23-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0ba23-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0ba23-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ba23-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0ba23-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0ba23-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0ba23-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ba23-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0ba23-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0ba23-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0ba23-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ba23-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ba23-119">**сдбкреатедатабасе**</span><span class="sxs-lookup"><span data-stu-id="0ba23-119">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
</dt> <dt>

[<span data-ttu-id="0ba23-120">**сдбопендатабасе**</span><span class="sxs-lookup"><span data-stu-id="0ba23-120">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




