---
title: Перечисление Хеадердисплайстиле
description: Используется Иресултсвиевер Хеадерстиле для установки или возврата текущего стиля заголовка.
ms.assetid: 13ae6317-d990-4ccf-83b3-275caf953611
keywords:
- Перечисление Хеадердисплайстиле. устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- HeaderDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc65b17fa61b799fc9ab8ea7cc1b01380a5843c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695012"
---
# <a name="headerdisplaystyle-enumeration"></a><span data-ttu-id="d70c0-104">Перечисление Хеадердисплайстиле</span><span class="sxs-lookup"><span data-stu-id="d70c0-104">HeaderDisplayStyle enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="d70c0-105">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d70c0-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d70c0-106">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="d70c0-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="d70c0-107">Используется [**иресултсвиевер:: хеадерстиле**](-search-2x-iresultsviewer-headerstyle.md) для установки или возврата текущего стиля заголовка.</span><span class="sxs-lookup"><span data-stu-id="d70c0-107">Used by [**IResultsViewer::HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md) to set or return the current header style.</span></span>

## <a name="syntax"></a><span data-ttu-id="d70c0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d70c0-108">Syntax</span></span>


```C++
typedef enum HeaderDisplayStyleEnum { 
  FullHeader     = 0,
  CompactHeader  = 1,
  NoHeader       = 2
} HeaderDisplayStyle;
```



## <a name="constants"></a><span data-ttu-id="d70c0-109">Константы</span><span class="sxs-lookup"><span data-stu-id="d70c0-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d70c0-110"><span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**фуллхеадер**</span><span class="sxs-lookup"><span data-stu-id="d70c0-110"><span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**FullHeader**</span></span>
</dt> <dd>

<span data-ttu-id="d70c0-111">Указывает или задает использование полных заголовков.</span><span class="sxs-lookup"><span data-stu-id="d70c0-111">Indicates or sets the use of full headers.</span></span>

</dd> <dt>

<span data-ttu-id="d70c0-112"><span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**компаксеадер**</span><span class="sxs-lookup"><span data-stu-id="d70c0-112"><span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**CompactHeader**</span></span>
</dt> <dd>

<span data-ttu-id="d70c0-113">Указывает или задает использование Compact Headers.</span><span class="sxs-lookup"><span data-stu-id="d70c0-113">Indicates or sets the use of compact headers.</span></span>

</dd> <dt>

<span data-ttu-id="d70c0-114"><span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="d70c0-114"><span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**NoHeader**</span></span>
</dt> <dd>

<span data-ttu-id="d70c0-115">Указывает или задает использование без заголовков.</span><span class="sxs-lookup"><span data-stu-id="d70c0-115">Indicates or sets the use of no headers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d70c0-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d70c0-116">Requirements</span></span>



| <span data-ttu-id="d70c0-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d70c0-117">Requirement</span></span> | <span data-ttu-id="d70c0-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d70c0-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d70c0-119">IDL</span><span class="sxs-lookup"><span data-stu-id="d70c0-119">IDL</span></span><br/> | <dl> <span data-ttu-id="d70c0-120"><dt>Вдсвиев. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d70c0-120"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





