---
title: Элемент автоархивации (Чаннеллоггингтипе)
description: Определяет, следует ли создавать новый файл журнала, когда текущий файл журнала достигает максимального размера.
ms.assetid: 708c5d44-d20b-437a-a01f-6182b244c736
keywords:
- Журнал событий элемента автоархивации
topic_type:
- apiref
api_name:
- autoBackup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d69c1a1c43be9d2376d94f39b3158e167f7bd13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535462"
---
# <a name="autobackup-channelloggingtype-element"></a><span data-ttu-id="a1cb2-104">Элемент автоархивации (Чаннеллоггингтипе)</span><span class="sxs-lookup"><span data-stu-id="a1cb2-104">autoBackup (ChannelLoggingType) Element</span></span>

<span data-ttu-id="a1cb2-105">Определяет, следует ли создавать новый файл журнала, когда текущий файл журнала достигает максимального размера.</span><span class="sxs-lookup"><span data-stu-id="a1cb2-105">Determines whether to create a new log file when the current log file reaches its maximum size.</span></span>

``` syntax
<xs:element name="autoBackup"
    type="boolean"
 />
```

<span data-ttu-id="a1cb2-106">Элемент **автоархивации** определяется сложным типом [**чаннеллоггингтипе**](eventmanifestschema-channelloggingtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a1cb2-106">The **autoBackup** element is defined by the [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1cb2-107">Требования</span><span class="sxs-lookup"><span data-stu-id="a1cb2-107">Requirements</span></span>



| <span data-ttu-id="a1cb2-108">Требование</span><span class="sxs-lookup"><span data-stu-id="a1cb2-108">Requirement</span></span> | <span data-ttu-id="a1cb2-109">Значение</span><span class="sxs-lookup"><span data-stu-id="a1cb2-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a1cb2-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1cb2-110">Minimum supported client</span></span><br/> | <span data-ttu-id="a1cb2-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a1cb2-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a1cb2-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1cb2-112">Minimum supported server</span></span><br/> | <span data-ttu-id="a1cb2-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a1cb2-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1cb2-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1cb2-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="a1cb2-115">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="a1cb2-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="a1cb2-116">**ведение журнала (Чаннелтипе)**</span><span class="sxs-lookup"><span data-stu-id="a1cb2-116">**logging (ChannelType)**</span></span>](eventmanifestschema-logging-channeltype-element.md)
</dt> </dl>

 

 





