---
title: Сложный тип Опкодетипе
description: Определяет операцию в компоненте приложения.
ms.assetid: d97953df-669b-4c55-b1a8-925022b339b7
keywords:
- Журнал событий сложных типов Опкодетипе
topic_type:
- apiref
api_name:
- OpcodeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5abaa11373086fe7f1237e10daf3e0a3df1cdb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137462"
---
# <a name="opcodetype-complex-type"></a><span data-ttu-id="cebda-104">Сложный тип Опкодетипе</span><span class="sxs-lookup"><span data-stu-id="cebda-104">OpcodeType Complex Type</span></span>

<span data-ttu-id="cebda-105">Определяет операцию в компоненте приложения.</span><span class="sxs-lookup"><span data-stu-id="cebda-105">Defines an operation within a component of the application.</span></span> <span data-ttu-id="cebda-106">Используется в сочетании с задачей для задания раздела приложения, в котором регистрируется событие.</span><span class="sxs-lookup"><span data-stu-id="cebda-106">Used in conjunction with a task to identify the section of the application that is logging the event.</span></span>

``` syntax
<xs:complexType name="OpcodeType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="mofValue"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="cebda-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="cebda-107">Attributes</span></span>



| <span data-ttu-id="cebda-108">Имя</span><span class="sxs-lookup"><span data-stu-id="cebda-108">Name</span></span>     | <span data-ttu-id="cebda-109">Тип</span><span class="sxs-lookup"><span data-stu-id="cebda-109">Type</span></span>                                                              | <span data-ttu-id="cebda-110">Описание</span><span class="sxs-lookup"><span data-stu-id="cebda-110">Description</span></span>                                                                                                                                                                                                                                                                                                          |
|----------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cebda-111">message</span><span class="sxs-lookup"><span data-stu-id="cebda-111">message</span></span>  | [<span data-ttu-id="cebda-112">**стртаблереф**</span><span class="sxs-lookup"><span data-stu-id="cebda-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="cebda-113">Локализованное отображаемое имя для кода операции.</span><span class="sxs-lookup"><span data-stu-id="cebda-113">The localized display name for the opcode.</span></span> <span data-ttu-id="cebda-114">Строка сообщения ссылается на локализованную строку в разделе " [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) " манифеста.</span><span class="sxs-lookup"><span data-stu-id="cebda-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                     |
| <span data-ttu-id="cebda-115">мофвалуе</span><span class="sxs-lookup"><span data-stu-id="cebda-115">mofValue</span></span> | [<span data-ttu-id="cebda-116">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="cebda-116">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="cebda-117">Зарезервировано только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="cebda-117">Reserved for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="cebda-118">name</span><span class="sxs-lookup"><span data-stu-id="cebda-118">name</span></span>     | <span data-ttu-id="cebda-119">**QName**</span><span class="sxs-lookup"><span data-stu-id="cebda-119">**QName**</span></span>                                                         | <span data-ttu-id="cebda-120">Имя кода операции.</span><span class="sxs-lookup"><span data-stu-id="cebda-120">The name of the opcode.</span></span> <span data-ttu-id="cebda-121">Это имя должно быть уникальным в пределах области этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="cebda-121">This name must be unique within the scope of this provider.</span></span> <br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="cebda-122">символ</span><span class="sxs-lookup"><span data-stu-id="cebda-122">symbol</span></span>   | [<span data-ttu-id="cebda-123">**ксимболтипе**</span><span class="sxs-lookup"><span data-stu-id="cebda-123">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="cebda-124">Символ, используемый для ссылки на код операции в приложении.</span><span class="sxs-lookup"><span data-stu-id="cebda-124">The symbol to use to reference the opcode in your application.</span></span> <span data-ttu-id="cebda-125">[**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ для создания константы для кода операции в файле заголовка, создаваемого компилятором.</span><span class="sxs-lookup"><span data-stu-id="cebda-125">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the opcode in the header file that the compiler generates.</span></span> <span data-ttu-id="cebda-126">Если не указать символ, компилятор создаст его.</span><span class="sxs-lookup"><span data-stu-id="cebda-126">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="cebda-127">значение</span><span class="sxs-lookup"><span data-stu-id="cebda-127">value</span></span>    | [<span data-ttu-id="cebda-128">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="cebda-128">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="cebda-129">Значение кода операции.</span><span class="sxs-lookup"><span data-stu-id="cebda-129">The opcode value.</span></span> <span data-ttu-id="cebda-130">Можно указать значения в диапазоне от 10 до 239.</span><span class="sxs-lookup"><span data-stu-id="cebda-130">You can specify values in the range 10 and 239.</span></span> <span data-ttu-id="cebda-131">Список предопределенных значений кодов операций см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="cebda-131">For a list of predefined opcode values, see Remarks.</span></span><br/>                                                                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="cebda-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cebda-132">Remarks</span></span>

<span data-ttu-id="cebda-133">Ниже приведены предопределенные значения кодов операций, которые можно использовать.</span><span class="sxs-lookup"><span data-stu-id="cebda-133">The following are the predefined opcode values that you can use.</span></span> <span data-ttu-id="cebda-134">Эти значения определяются в Winmeta.xml файле, включенном в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="cebda-134">These values are defined in the Winmeta.xml file that is included in the Windows SDK.</span></span>



| <span data-ttu-id="cebda-135">Имя</span><span class="sxs-lookup"><span data-stu-id="cebda-135">Name</span></span>          | <span data-ttu-id="cebda-136">Значение</span><span class="sxs-lookup"><span data-stu-id="cebda-136">Value</span></span> | <span data-ttu-id="cebda-137">Символ</span><span class="sxs-lookup"><span data-stu-id="cebda-137">Symbol</span></span>                      | <span data-ttu-id="cebda-138">Описание</span><span class="sxs-lookup"><span data-stu-id="cebda-138">Description</span></span>                                                                                            |
|---------------|-------|-----------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cebda-139">Win: info</span><span class="sxs-lookup"><span data-stu-id="cebda-139">win:Info</span></span>      | <span data-ttu-id="cebda-140">0</span><span class="sxs-lookup"><span data-stu-id="cebda-140">0</span></span>     | <span data-ttu-id="cebda-141">\_сведения о коде операции WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="cebda-141">WINEVENT\_OPCODE\_INFO</span></span>      | <span data-ttu-id="cebda-142">Информационное событие.</span><span class="sxs-lookup"><span data-stu-id="cebda-142">An informational event.</span></span>                                                                                |
| <span data-ttu-id="cebda-143">Win: начало</span><span class="sxs-lookup"><span data-stu-id="cebda-143">win:Start</span></span>     | <span data-ttu-id="cebda-144">1</span><span class="sxs-lookup"><span data-stu-id="cebda-144">1</span></span>     | <span data-ttu-id="cebda-145">\_начало кода операции WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="cebda-145">WINEVENT\_OPCODE\_START</span></span>     | <span data-ttu-id="cebda-146">Событие, представляющее Запуск действия.</span><span class="sxs-lookup"><span data-stu-id="cebda-146">An event that represents starting an activity.</span></span>                                                         |
| <span data-ttu-id="cebda-147">Win: завершение</span><span class="sxs-lookup"><span data-stu-id="cebda-147">win:Stop</span></span>      | <span data-ttu-id="cebda-148">2</span><span class="sxs-lookup"><span data-stu-id="cebda-148">2</span></span>     | <span data-ttu-id="cebda-149">WINEVENT \_ код операции \_ завершения</span><span class="sxs-lookup"><span data-stu-id="cebda-149">WINEVENT\_OPCODE\_STOP</span></span>      | <span data-ttu-id="cebda-150">Событие, представляющее остановку действия.</span><span class="sxs-lookup"><span data-stu-id="cebda-150">An event that represents stopping an activity.</span></span> <span data-ttu-id="cebda-151">Событие соответствует последнему непарному событию запуска.</span><span class="sxs-lookup"><span data-stu-id="cebda-151">The event corresponds to the last unpaired start event.</span></span> |
| <span data-ttu-id="cebda-152">Win: начало контроллера домена \_</span><span class="sxs-lookup"><span data-stu-id="cebda-152">win:DC\_Start</span></span> | <span data-ttu-id="cebda-153">3</span><span class="sxs-lookup"><span data-stu-id="cebda-153">3</span></span>     | <span data-ttu-id="cebda-154">WINEVENT \_ код \_ операции \_ запуска контроллера домена</span><span class="sxs-lookup"><span data-stu-id="cebda-154">WINEVENT\_OPCODE\_DC\_START</span></span> | <span data-ttu-id="cebda-155">Событие, представляющее Запуск сбора данных.</span><span class="sxs-lookup"><span data-stu-id="cebda-155">An event that represents data collection starting.</span></span> <span data-ttu-id="cebda-156">Это типы событий очистки.</span><span class="sxs-lookup"><span data-stu-id="cebda-156">These are rundown event types.</span></span>                      |
| <span data-ttu-id="cebda-157">выигрыш: завершение контроллера домена \_</span><span class="sxs-lookup"><span data-stu-id="cebda-157">win:DC\_Stop</span></span>  | <span data-ttu-id="cebda-158">4</span><span class="sxs-lookup"><span data-stu-id="cebda-158">4</span></span>     | <span data-ttu-id="cebda-159">WINEVENT \_ код \_ операции \_ завершения контроллера домена</span><span class="sxs-lookup"><span data-stu-id="cebda-159">WINEVENT\_OPCODE\_DC\_STOP</span></span>  | <span data-ttu-id="cebda-160">Событие, представляющее остановку сбора данных.</span><span class="sxs-lookup"><span data-stu-id="cebda-160">An event that represents data collection stopping.</span></span> <span data-ttu-id="cebda-161">Это типы событий очистки.</span><span class="sxs-lookup"><span data-stu-id="cebda-161">These are rundown event types.</span></span>                      |
| <span data-ttu-id="cebda-162">Win: Extension</span><span class="sxs-lookup"><span data-stu-id="cebda-162">win:Extension</span></span> | <span data-ttu-id="cebda-163">5</span><span class="sxs-lookup"><span data-stu-id="cebda-163">5</span></span>     | <span data-ttu-id="cebda-164">\_расширение кода операции WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="cebda-164">WINEVENT\_OPCODE\_EXTENSION</span></span> | <span data-ttu-id="cebda-165">Событие расширения.</span><span class="sxs-lookup"><span data-stu-id="cebda-165">An extension event.</span></span>                                                                                    |
| <span data-ttu-id="cebda-166">Win: ответ</span><span class="sxs-lookup"><span data-stu-id="cebda-166">win:Reply</span></span>     | <span data-ttu-id="cebda-167">6</span><span class="sxs-lookup"><span data-stu-id="cebda-167">6</span></span>     | <span data-ttu-id="cebda-168">\_Ответ кода операции WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="cebda-168">WINEVENT\_OPCODE\_REPLY</span></span>     | <span data-ttu-id="cebda-169">Событие ответа.</span><span class="sxs-lookup"><span data-stu-id="cebda-169">A reply event.</span></span>                                                                                         |
| <span data-ttu-id="cebda-170">Win: Resume</span><span class="sxs-lookup"><span data-stu-id="cebda-170">win:Resume</span></span>    | <span data-ttu-id="cebda-171">7</span><span class="sxs-lookup"><span data-stu-id="cebda-171">7</span></span>     | <span data-ttu-id="cebda-172">\_возобновление кода операции WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="cebda-172">WINEVENT\_OPCODE\_RESUME</span></span>    | <span data-ttu-id="cebda-173">Событие, представляющее возобновление действия после приостановки.</span><span class="sxs-lookup"><span data-stu-id="cebda-173">An event that represents an activity resuming after being suspended.</span></span>                                   |
| <span data-ttu-id="cebda-174">Win: Suspend</span><span class="sxs-lookup"><span data-stu-id="cebda-174">win:Suspend</span></span>   | <span data-ttu-id="cebda-175">8</span><span class="sxs-lookup"><span data-stu-id="cebda-175">8</span></span>     | <span data-ttu-id="cebda-176">Приостановка WINEVENT \_ кода операции \_</span><span class="sxs-lookup"><span data-stu-id="cebda-176">WINEVENT\_OPCODE\_SUSPEND</span></span>   | <span data-ttu-id="cebda-177">Событие, представляющее действие, которое приостанавливается в ожидании завершения другого действия.</span><span class="sxs-lookup"><span data-stu-id="cebda-177">An event that represents the activity being suspended pending another activity's completion.</span></span>           |
| <span data-ttu-id="cebda-178">Win: send</span><span class="sxs-lookup"><span data-stu-id="cebda-178">win:Send</span></span>      | <span data-ttu-id="cebda-179">9</span><span class="sxs-lookup"><span data-stu-id="cebda-179">9</span></span>     | <span data-ttu-id="cebda-180">\_Отправка кода операции WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="cebda-180">WINEVENT\_OPCODE\_SEND</span></span>      | <span data-ttu-id="cebda-181">Событие, представляющее передачу действия в другой компонент.</span><span class="sxs-lookup"><span data-stu-id="cebda-181">An event that represents transferring activity to another component.</span></span>                                   |
| <span data-ttu-id="cebda-182">выигрыш: получение</span><span class="sxs-lookup"><span data-stu-id="cebda-182">win:Receive</span></span>   | <span data-ttu-id="cebda-183">240</span><span class="sxs-lookup"><span data-stu-id="cebda-183">240</span></span>   | <span data-ttu-id="cebda-184">\_Получение кода операции WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="cebda-184">WINEVENT\_OPCODE\_RECEIVE</span></span>   | <span data-ttu-id="cebda-185">Событие, представляющее получение действия, передаваемой из другого компонента.</span><span class="sxs-lookup"><span data-stu-id="cebda-185">An event that represents receiving an activity transfer from another component.</span></span>                        |



 

## <a name="requirements"></a><span data-ttu-id="cebda-186">Требования</span><span class="sxs-lookup"><span data-stu-id="cebda-186">Requirements</span></span>



| <span data-ttu-id="cebda-187">Требование</span><span class="sxs-lookup"><span data-stu-id="cebda-187">Requirement</span></span> | <span data-ttu-id="cebda-188">Значение</span><span class="sxs-lookup"><span data-stu-id="cebda-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cebda-189">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cebda-189">Minimum supported client</span></span><br/> | <span data-ttu-id="cebda-190">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cebda-190">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cebda-191">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cebda-191">Minimum supported server</span></span><br/> | <span data-ttu-id="cebda-192">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cebda-192">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





