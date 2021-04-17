---
title: Сложный тип Евентстипе
description: Содержит список поставщиков, определенных в манифесте. | Сложный тип Евентстипе
ms.assetid: 43f9f577-eae0-45c5-aaf0-5a6df28d3b79
keywords:
- Журнал событий сложных типов Евентстипе
topic_type:
- apiref
api_name:
- EventsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36500aa037c8e33a48b4f9dd6e38e46eaac58da2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694006"
---
# <a name="eventstype-complex-type"></a><span data-ttu-id="93033-105">Сложный тип Евентстипе</span><span class="sxs-lookup"><span data-stu-id="93033-105">EventsType Complex Type</span></span>

<span data-ttu-id="93033-106">Содержит список поставщиков, определенных в манифесте.</span><span class="sxs-lookup"><span data-stu-id="93033-106">Contains a list of providers that are defined in the manifest.</span></span>

``` syntax
<xs:complexType name="EventsType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="provider"
            type="ProviderType"
            maxOccurs="unbounded"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="93033-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="93033-107">Child elements</span></span>

| <span data-ttu-id="93033-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="93033-108">Element</span></span> | <span data-ttu-id="93033-109">Тип</span><span class="sxs-lookup"><span data-stu-id="93033-109">Type</span></span> | <span data-ttu-id="93033-110">Описание</span><span class="sxs-lookup"><span data-stu-id="93033-110">Description</span></span> |
|---------|------|-------------|
| <span data-ttu-id="93033-111">message</span><span class="sxs-lookup"><span data-stu-id="93033-111">message</span></span> |      | <span data-ttu-id="93033-112">Определяет строку сообщения.</span><span class="sxs-lookup"><span data-stu-id="93033-112">Defines a message string.</span></span> |
| <span data-ttu-id="93033-113">мессажетабле</span><span class="sxs-lookup"><span data-stu-id="93033-113">messageTable</span></span> | | <span data-ttu-id="93033-114">Определяет список строк сообщений.</span><span class="sxs-lookup"><span data-stu-id="93033-114">Defines a list of message strings.</span></span> <span data-ttu-id="93033-115">Не следует использовать таблицу сообщений, за исключением следующих случаев, когда необходимо определить таблицу сообщений для явного назначения номеров ресурсов строкам сообщений.</span><span class="sxs-lookup"><span data-stu-id="93033-115">You should not have to use a message table except in the following cases where you must define a message table to explicitly assign resource numbers to message strings.</span></span> <ul><li><span data-ttu-id="93033-116">Выполняется миграция из текстового файла сообщения (. MC) в манифест, но все еще записываются события в приложения и системные каналы, чтобы устаревшие потребители продолжали потреблять события.</span><span class="sxs-lookup"><span data-stu-id="93033-116">You are migrating from a message text (.mc) file to a manifest but are still writing events to the application and system channels, so that legacy consumers to continue consuming the events.</span></span> <span data-ttu-id="93033-117">Чтобы сделать эту работу, идентификаторы ресурсов для строк сообщений, определенных в манифесте, должны совпадать с идентификаторами событий.</span><span class="sxs-lookup"><span data-stu-id="93033-117">To make this work, the resource identifiers for the message strings defined in the manifest must be the same as the event identifiers.</span></span> <span data-ttu-id="93033-118">Однако компилятор сообщений автоматически назначает идентификаторы ресурсов строкам сообщений.</span><span class="sxs-lookup"><span data-stu-id="93033-118">However, the message compiler automatically assigns resource identifiers to the message strings.</span></span> <span data-ttu-id="93033-119">Чтобы переопределить компилятор, используйте таблицу сообщений и присвойте атрибуту Value идентификатор события и атрибут Message для ссылки на строку в таблице строк в разделе локализации манифеста.</span><span class="sxs-lookup"><span data-stu-id="93033-119">To override the compiler, use the message table and set the value attribute to the event identifier and the message attribute to refer to a string in the string table in the localization section of the manifest.</span></span></li><li><span data-ttu-id="93033-120">Если требуется определить более 16 поставщиков, необходимо включить таблицу сообщений, которую семнадцатого и поставщики должны использовать для назначения значений ресурсов для строк сообщений, которые они определяют.</span><span class="sxs-lookup"><span data-stu-id="93033-120">If you want to identify more than 16 providers, you must include the message table that the seventeenth and on providers must use to assign resource values for the message strings that they define.</span></span> <span data-ttu-id="93033-121">Если поставщик ссылается на строки сообщений, определенные поставщиками от 1 до 16, эти строки сообщений не включаются в таблицу сообщений.</span><span class="sxs-lookup"><span data-stu-id="93033-121">If the provider references message strings that providers 1 through 16 defined, you do not include those message strings in the message table.</span></span></li></ul>|
| [<span data-ttu-id="93033-122">**поставщики**</span><span class="sxs-lookup"><span data-stu-id="93033-122">**provider**</span></span>](eventmanifestschema-provider-eventstype-element.md) | [<span data-ttu-id="93033-123">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="93033-123">**ProviderType**</span></span>](eventmanifestschema-providertype-complextype.md) | <span data-ttu-id="93033-124">Список поставщиков, которые необходимо определить.</span><span class="sxs-lookup"><span data-stu-id="93033-124">A list of providers that you want to define.</span></span> |

## <a name="attributes"></a><span data-ttu-id="93033-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="93033-125">Attributes</span></span>

| <span data-ttu-id="93033-126">Имя</span><span class="sxs-lookup"><span data-stu-id="93033-126">Name</span></span>    | <span data-ttu-id="93033-127">Тип</span><span class="sxs-lookup"><span data-stu-id="93033-127">Type</span></span>                                                             | <span data-ttu-id="93033-128">Описание</span><span class="sxs-lookup"><span data-stu-id="93033-128">Description</span></span>                                                                            |
|---------|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93033-129">message</span><span class="sxs-lookup"><span data-stu-id="93033-129">message</span></span> | [<span data-ttu-id="93033-130">**стртаблереф**</span><span class="sxs-lookup"><span data-stu-id="93033-130">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="93033-131">Ссылка на локализованную строку в таблице строк.</span><span class="sxs-lookup"><span data-stu-id="93033-131">A reference to the localized string in the string table.</span></span>                               |
| <span data-ttu-id="93033-132">mid</span><span class="sxs-lookup"><span data-stu-id="93033-132">mid</span></span>     | <span data-ttu-id="93033-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="93033-133">xs:string</span></span>                                                        | <span data-ttu-id="93033-134">Не используется.</span><span class="sxs-lookup"><span data-stu-id="93033-134">Not used.</span></span>                                                                              |
| <span data-ttu-id="93033-135">символ</span><span class="sxs-lookup"><span data-stu-id="93033-135">symbol</span></span>  | [<span data-ttu-id="93033-136">**ксимболтипе**</span><span class="sxs-lookup"><span data-stu-id="93033-136">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="93033-137">Символьное имя, создаваемое компилятором сообщений для этой строки сообщения.</span><span class="sxs-lookup"><span data-stu-id="93033-137">The symbolic name that you want the message compiler to create for this message string.</span></span>|
| <span data-ttu-id="93033-138">значение</span><span class="sxs-lookup"><span data-stu-id="93033-138">value</span></span>   | [<span data-ttu-id="93033-139">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="93033-139">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="93033-140">Число, используемое в качестве идентификатора сообщения для данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="93033-140">The number to use as the message identifier for this message.</span></span>                          |


## <a name="remarks"></a><span data-ttu-id="93033-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93033-141">Remarks</span></span>

<span data-ttu-id="93033-142">Практический лимит количества поставщиков, которые можно определить в манифесте, составляет 16 поставщиков.</span><span class="sxs-lookup"><span data-stu-id="93033-142">The practical limit of the number of providers that you can define in a manifest is 16 providers.</span></span> <span data-ttu-id="93033-143">При указании более 16 поставщиков необходимо использовать таблицу сообщений для явного присвоения номеров ресурсов строкам сообщений, на которые ссылается поставщик.</span><span class="sxs-lookup"><span data-stu-id="93033-143">If you specify more than 16 providers, you must use a message table to explicitly assign resource numbers to the message strings that the provider references.</span></span> <span data-ttu-id="93033-144">Дополнительные сведения см. в элементе Message выше.</span><span class="sxs-lookup"><span data-stu-id="93033-144">For more details, see the message element above.</span></span>

## <a name="requirements"></a><span data-ttu-id="93033-145">Требования</span><span class="sxs-lookup"><span data-stu-id="93033-145">Requirements</span></span>

| <span data-ttu-id="93033-146">Требование</span><span class="sxs-lookup"><span data-stu-id="93033-146">Requirement</span></span> | <span data-ttu-id="93033-147">Значение</span><span class="sxs-lookup"><span data-stu-id="93033-147">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="93033-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93033-148">Minimum supported client</span></span> | <span data-ttu-id="93033-149">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="93033-149">Windows Vista \[desktop apps only\]</span></span>       |
| <span data-ttu-id="93033-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93033-150">Minimum supported server</span></span> | <span data-ttu-id="93033-151">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="93033-151">Windows Server 2008 \[desktop apps only\]</span></span> |
