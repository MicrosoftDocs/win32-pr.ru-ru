---
title: opcode, элемент (Опкоделисттипе)
description: Содержит числовое значение, которое определяет действие или точку в действии, которое приложение выполняло при возникновении события (например, инициализация или закрытие).
ms.assetid: 8c5cfbd3-6a74-452c-a12f-41d663426e2c
keywords:
- Журнал событий элемента кода операции
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9d02b77b4a36bac26d52d7bf8d849eab8731d27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137463"
---
# <a name="opcode-opcodelisttype-element"></a><span data-ttu-id="6a4ea-104">opcode, элемент (Опкоделисттипе)</span><span class="sxs-lookup"><span data-stu-id="6a4ea-104">opcode (OpcodeListType) Element</span></span>

<span data-ttu-id="6a4ea-105">Содержит числовое значение, которое определяет действие или точку в действии, которое приложение выполняло при возникновении события (например, инициализация или закрытие).</span><span class="sxs-lookup"><span data-stu-id="6a4ea-105">Contains a numeric value that identifies the activity or a point within an activity that the application was performing when it raised the event (for example, initialization or closing).</span></span>

``` syntax
<xs:element name="opcode"
    type="OpcodeType"
 />
```

<span data-ttu-id="6a4ea-106">Элемент **кода операции** определяется сложным типом [**опкоделисттипе**](eventmanifestschema-opcodelisttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6a4ea-106">The **opcode** element is defined by the [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a4ea-107">Требования</span><span class="sxs-lookup"><span data-stu-id="6a4ea-107">Requirements</span></span>



| <span data-ttu-id="6a4ea-108">Требование</span><span class="sxs-lookup"><span data-stu-id="6a4ea-108">Requirement</span></span> | <span data-ttu-id="6a4ea-109">Значение</span><span class="sxs-lookup"><span data-stu-id="6a4ea-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6a4ea-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a4ea-110">Minimum supported client</span></span><br/> | <span data-ttu-id="6a4ea-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a4ea-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6a4ea-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a4ea-112">Minimum supported server</span></span><br/> | <span data-ttu-id="6a4ea-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6a4ea-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6a4ea-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a4ea-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="6a4ea-115">**Родительские элементы**</span><span class="sxs-lookup"><span data-stu-id="6a4ea-115">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="6a4ea-116">**коды операций (TaskType)**</span><span class="sxs-lookup"><span data-stu-id="6a4ea-116">**opcodes (TaskType)**</span></span>](eventmanifestschema-opcodes-tasktype-element.md)
</dt> <dt>

[<span data-ttu-id="6a4ea-117">**коды операций (ProviderType)**</span><span class="sxs-lookup"><span data-stu-id="6a4ea-117">**opcodes (ProviderType)**</span></span>](eventmanifestschema-opcodes-providertype-element.md)
</dt> <dt>

[<span data-ttu-id="6a4ea-118">**коды операций (Метадататипе)**</span><span class="sxs-lookup"><span data-stu-id="6a4ea-118">**opcodes (MetadataType)**</span></span>](eventmanifestschema-opcodes-metadatatype-element.md)
</dt> </dl>

 

 





