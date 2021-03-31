---
title: Сложный тип Импортчаннелтипе
description: Определяет канал, который был определен другим поставщиком или манифестом, содержащим раздел метаданных.
ms.assetid: da14d837-0ed8-4d85-9820-46c77753768d
keywords:
- Журнал событий сложных типов Импортчаннелтипе
topic_type:
- apiref
api_name:
- ImportChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7500d52179c3282c7f15dcdd5dd5a32620bbc076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135822"
---
# <a name="importchanneltype-complex-type"></a><span data-ttu-id="f404f-104">Сложный тип Импортчаннелтипе</span><span class="sxs-lookup"><span data-stu-id="f404f-104">ImportChannelType Complex Type</span></span>

<span data-ttu-id="f404f-105">Определяет канал, который был определен другим поставщиком или манифестом, содержащим раздел метаданных.</span><span class="sxs-lookup"><span data-stu-id="f404f-105">Identifies a channel that has been defined by another provider or in a manifest that contains a metadata section.</span></span>

``` syntax
<xs:complexType name="ImportChannelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="chid"
                type="token"
                use="optional"
             />
            <xs:attribute name="name"
                type="anyURI"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="f404f-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f404f-106">Attributes</span></span>



| <span data-ttu-id="f404f-107">Имя</span><span class="sxs-lookup"><span data-stu-id="f404f-107">Name</span></span>   | <span data-ttu-id="f404f-108">Тип</span><span class="sxs-lookup"><span data-stu-id="f404f-108">Type</span></span>                                                              | <span data-ttu-id="f404f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f404f-109">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f404f-110">чид</span><span class="sxs-lookup"><span data-stu-id="f404f-110">chid</span></span>   | <span data-ttu-id="f404f-111">token</span><span class="sxs-lookup"><span data-stu-id="f404f-111">token</span></span>                                                             | <span data-ttu-id="f404f-112">Идентификатор, который уникальным образом идентифицирует канал в списке каналов, определяемых или импортируемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="f404f-112">An identifier that uniquely identifies the channel in the list of channels that the provider defines or imports.</span></span> <span data-ttu-id="f404f-113">Используйте это значение при ссылке на этот канал в определении события.</span><span class="sxs-lookup"><span data-stu-id="f404f-113">Use this value when referencing this channel in an event definition.</span></span> <span data-ttu-id="f404f-114">Если идентификатор канала не указан, используйте имя канала для ссылки на этот канал в определении события.</span><span class="sxs-lookup"><span data-stu-id="f404f-114">If you do not specify a channel identifier, use the channel's name to reference this channel in an event definition.</span></span><br/>  |
| <span data-ttu-id="f404f-115">name</span><span class="sxs-lookup"><span data-stu-id="f404f-115">name</span></span>   | <span data-ttu-id="f404f-116">anyURI</span><span class="sxs-lookup"><span data-stu-id="f404f-116">anyURI</span></span>                                                            | <span data-ttu-id="f404f-117">Имя импортируемого канала.</span><span class="sxs-lookup"><span data-stu-id="f404f-117">The name of the channel to import.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="f404f-118">символ</span><span class="sxs-lookup"><span data-stu-id="f404f-118">symbol</span></span> | [<span data-ttu-id="f404f-119">**ксимболтипе**</span><span class="sxs-lookup"><span data-stu-id="f404f-119">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="f404f-120">Символ, используемый для ссылки на канал в приложении.</span><span class="sxs-lookup"><span data-stu-id="f404f-120">The symbol to use to reference the channel in your application.</span></span> <span data-ttu-id="f404f-121">[**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ, чтобы создать константу для канала в файле заголовка, создаваемом компилятором.</span><span class="sxs-lookup"><span data-stu-id="f404f-121">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the channel in the header file that the compiler generates.</span></span> <span data-ttu-id="f404f-122">Если не указать символ, компилятор создаст его.</span><span class="sxs-lookup"><span data-stu-id="f404f-122">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f404f-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f404f-123">Remarks</span></span>

<span data-ttu-id="f404f-124">Манифест, в котором был определен импортированный канал, должен быть установлен до того, как поставщик запишет события. в противном случае события не могут быть записаны в канал (операция записи выполняется правильно, события просто не записываются в канал).</span><span class="sxs-lookup"><span data-stu-id="f404f-124">The manifest that defined the imported channel must be installed before your provider writes events; otherwise, the events cannot be written to the channel (the write operation succeeds, the events are simply not written to the channel).</span></span>

## <a name="requirements"></a><span data-ttu-id="f404f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="f404f-125">Requirements</span></span>



| <span data-ttu-id="f404f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="f404f-126">Requirement</span></span> | <span data-ttu-id="f404f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="f404f-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f404f-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f404f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f404f-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f404f-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f404f-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f404f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f404f-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f404f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





