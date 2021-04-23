---
description: Определяет поставщик и предоставляемые им счетчики.
ms.assetid: 85299b01-5679-40f8-8aec-5c2ff8d7cfc8
title: Сложный тип поставщика
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eec52139710d0ffafe06f22504a735e59312818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909715"
---
# <a name="provider-complex-type"></a><span data-ttu-id="2a693-103">Сложный тип поставщика</span><span class="sxs-lookup"><span data-stu-id="2a693-103">provider Complex Type</span></span>

<span data-ttu-id="2a693-104">Определяет поставщик и предоставляемые им счетчики.</span><span class="sxs-lookup"><span data-stu-id="2a693-104">Defines a provider and the counters that it provides.</span></span>

``` syntax
<xs:complexType name="provider">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="counterSet"
            type="man:counterSet"
        >
            <xs:key name="uniqueCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@id"
                 />
            </xs:key>
            <xs:unique name="uniqueCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:unique>
            <xs:keyref name="existBaseID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@baseID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfTimeID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfTimeID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfFreqID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfFreqID"
                 />
            </xs:keyref>
            <xs:keyref name="existMultiCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@multiCounterID"
                 />
            </xs:keyref>
            <xs:key name="uniqueStructNames">
                <xs:selector
                    xpath="./man:structs/man:struct"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:key>
            <xs:keyref name="existCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@struct"
                 />
            </xs:keyref>
        </xs:element>
    </xs:choice>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="callback"
        use="optional"
        default="default"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="custom"
                 />
                <xs:enumeration
                    value="default"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerGuid"
        type="man:GUIDType"
        use="required"
     />
    <xs:attribute name="applicationIdentity"
        type="xs:string"
        use="required"
     />
    <xs:attribute name="providerType"
        use="optional"
        default="userMode"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="userMode"
                 />
                <xs:enumeration
                    value="kernelMode"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerName"
        type="xs:string"
        use="optional"
        default="Counters"
     />
    <xs:attribute name="resourceBase"
        type="man:UInt32Type"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="2a693-105">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2a693-105">Child elements</span></span>



| <span data-ttu-id="2a693-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="2a693-106">Element</span></span>        | <span data-ttu-id="2a693-107">Тип</span><span class="sxs-lookup"><span data-stu-id="2a693-107">Type</span></span>                                                                   | <span data-ttu-id="2a693-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2a693-108">Description</span></span>                                                                                 |
|----------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a693-109">**counterSet**</span><span class="sxs-lookup"><span data-stu-id="2a693-109">**counterSet**</span></span> | [<span data-ttu-id="2a693-110">**Man: CounterSet**</span><span class="sxs-lookup"><span data-stu-id="2a693-110">**man:counterSet**</span></span>](performance-counters-counterset-complex-type.md) | <span data-ttu-id="2a693-111">Определяет набор счетчиков, который содержит один или несколько логически связанных счетчиков.</span><span class="sxs-lookup"><span data-stu-id="2a693-111">Identifies the counter set that contains one or more logically related counters.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="2a693-112">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2a693-112">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a693-113">Имя</span><span class="sxs-lookup"><span data-stu-id="2a693-113">Name</span></span></th>
<th><span data-ttu-id="2a693-114">Тип</span><span class="sxs-lookup"><span data-stu-id="2a693-114">Type</span></span></th>
<th><span data-ttu-id="2a693-115">Описание</span><span class="sxs-lookup"><span data-stu-id="2a693-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a693-116">аппликатионидентити</span><span class="sxs-lookup"><span data-stu-id="2a693-116">applicationIdentity</span></span></td>
<td><span data-ttu-id="2a693-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="2a693-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="2a693-118">Имя двоичного файла, содержащего локализованные строки ресурсов: exe или DLL (не включайте в двоичный файл путь к файлу).</span><span class="sxs-lookup"><span data-stu-id="2a693-118">The name of the binary file that contains the localized resource strings, either an .exe or .dll file (do not include the path to the binary).</span></span><br/> <span data-ttu-id="2a693-119">Служебная программа Lodctr.exe использует путь из необязательного параметра [<em>path</em>] для поиска двоичного файла.</span><span class="sxs-lookup"><span data-stu-id="2a693-119">The Lodctr.exe utility uses the path from the optional [<em>path</em>] parameter to search for the binary file.</span></span> <span data-ttu-id="2a693-120">Например, <strong>lodctr</strong> [<strong>/m:</strong><em>manifest</em> [<em>путь</em>]].</span><span class="sxs-lookup"><span data-stu-id="2a693-120">For example, <strong>lodctr</strong> [<strong>/m:</strong><em>manifest</em> [<em>path</em>]].</span></span> <span data-ttu-id="2a693-121">Если параметр [<em>path</em>] не включен, Lodctr.exe выполняет поиск в папке, содержащей манифест.</span><span class="sxs-lookup"><span data-stu-id="2a693-121">If you do not include the [<em>path</em>] parameter, Lodctr.exe searches the folder that contains the manifest.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a693-122">обратный вызов</span><span class="sxs-lookup"><span data-stu-id="2a693-122">callback</span></span></td>

<td><span data-ttu-id="2a693-123">Этот атрибут указывает, что вы хотите получить уведомление, когда потребитель выполняет определенные действия.</span><span class="sxs-lookup"><span data-stu-id="2a693-123">This attribute indicates that you want to receive notification when a consumer performs certain actions.</span></span> <br/> <span data-ttu-id="2a693-124">Если включить этот атрибут, средство КТРПП использует альтернативную сигнатуру <a href="counterinitialize.md"><strong>каунтеринитиализе</strong></a> Function, которая используется для передачи имени функции, реализующей функцию обратного вызова <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>контролкаллбакк</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2a693-124">If you include this attribute, the CTRPP tool uses the alternate <a href="counterinitialize.md"><strong>CounterInitialize</strong></a> function signature, which you use to pass in the name of your function that implements the <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> callback function.</span></span><br/> <span data-ttu-id="2a693-125">В качестве альтернативы указанию этого атрибута можно использовать аргумент <strong>-нотификатионкаллбакк</strong><a href="ctrpp.md">КТРПП</a> .</span><span class="sxs-lookup"><span data-stu-id="2a693-125">As an alternative to specifying this attribute, you can use the <strong>-NotificationCallback</strong><a href="ctrpp.md">CTRPP</a> argument.</span></span><br/> <span data-ttu-id="2a693-126"><strong>Windows Vista:</strong> Единственным допустимым значением для этого атрибута является &quot; Custom &quot; .</span><span class="sxs-lookup"><span data-stu-id="2a693-126"><strong>Windows Vista:</strong> The only valid value for this attribute is &quot;custom&quot;.</span></span> <span data-ttu-id="2a693-127">Служебная программа <a href="ctrpp.md">КТРПП</a> создает шаблон для функции обратного вызова <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>контролкаллбакк</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2a693-127">The <a href="ctrpp.md">CTRPP</a> utility generates the template for a <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> callback function.</span></span> <span data-ttu-id="2a693-128">Шаблон включается в файл c, созданный КТРПП.</span><span class="sxs-lookup"><span data-stu-id="2a693-128">The template is included in the .c file that CTRPP generated.</span></span> <br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a693-129">провидергуид</span><span class="sxs-lookup"><span data-stu-id="2a693-129">providerGuid</span></span></td>
<td><span data-ttu-id="2a693-130"><a href="performance-counters-guidtype-simple-type.md"><strong>мужчина: Гуидтипе</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a693-130"><a href="performance-counters-guidtype-simple-type.md"><strong>man:GUIDType</strong></a></span></span></td>
<td><span data-ttu-id="2a693-131">Строковый идентификатор GUID, однозначно определяющий поставщика в манифесте.</span><span class="sxs-lookup"><span data-stu-id="2a693-131">String GUID that uniquely identifies the provider in the manifest.</span></span> <span data-ttu-id="2a693-132">Идентификатор GUID должен быть уникальным в пределах манифеста.</span><span class="sxs-lookup"><span data-stu-id="2a693-132">The GUID must be unique within the manifest.</span></span><br/> <span data-ttu-id="2a693-133">Новый GUID необходимо указывать только при изменении версии приложения (если поддерживаются параллельные установки).</span><span class="sxs-lookup"><span data-stu-id="2a693-133">You need to provide a new GUID only when the version of the application changes (if you support side-by-side installations).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a693-134">providerName</span><span class="sxs-lookup"><span data-stu-id="2a693-134">providerName</span></span></td>
<td><span data-ttu-id="2a693-135"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="2a693-135"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="2a693-136">Имя, используемое для создания имени класса Win32_PerfRawData WMI.</span><span class="sxs-lookup"><span data-stu-id="2a693-136">The name that is used to create the WMI Win32_PerfRawData class name.</span></span> <span data-ttu-id="2a693-137">Если имя не указано, &quot; счетчики &quot; будут использоваться в качестве имени класса.</span><span class="sxs-lookup"><span data-stu-id="2a693-137">If you do not specify a name, &quot;Counters&quot; is used as the name of the class.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a693-138">providerType</span><span class="sxs-lookup"><span data-stu-id="2a693-138">providerType</span></span></td>

<td><span data-ttu-id="2a693-139">Определяет, является ли поставщик поставщиком пользовательского режима, поставщиком режима ядра или поставщиком драйвера.</span><span class="sxs-lookup"><span data-stu-id="2a693-139">Identifies whether the provider is a user-mode provider, kernel-mode provider, or driver provider.</span></span> <span data-ttu-id="2a693-140">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="2a693-140">Possible values are as follows.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2a693-141">Термин</span><span class="sxs-lookup"><span data-stu-id="2a693-141">Term</span></span></th>
<th><span data-ttu-id="2a693-142">Описание</span><span class="sxs-lookup"><span data-stu-id="2a693-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a693-143"><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>Пользовательском</span><span class="sxs-lookup"><span data-stu-id="2a693-143"><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>userMode</span></span><br/></td>
<td><span data-ttu-id="2a693-144">Укажите этот режим для компонента пользовательского режима, такого как приложение, Библиотека DLL или драйвер пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="2a693-144">Specify this mode for a user-mode component such as an application, a DLL, or a user-mode driver.</span></span> <span data-ttu-id="2a693-145">Типичными расширениями для компонентов пользовательского режима являются exe-или DLL-файлы.</span><span class="sxs-lookup"><span data-stu-id="2a693-145">The typical extensions for user-mode components are .exe or .dll.</span></span> <span data-ttu-id="2a693-146">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2a693-146">This is the default.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a693-147"><span id="kernel"></span><span id="KERNEL"></span>версиями</span><span class="sxs-lookup"><span data-stu-id="2a693-147"><span id="kernel"></span><span id="KERNEL"></span>kernel</span></span><br/></td>
<td><span data-ttu-id="2a693-148">Укажите этот режим для компонента режима ядра, такого как драйвер WDM или ВДФ.</span><span class="sxs-lookup"><span data-stu-id="2a693-148">Specify this mode for a kernel-mode component such as a WDM or WDF driver.</span></span> <span data-ttu-id="2a693-149">Стандартным расширением для компонентов режима ядра является. sys.</span><span class="sxs-lookup"><span data-stu-id="2a693-149">The typical extension for kernel-mode components is .sys.</span></span><br/> <span data-ttu-id="2a693-150"><strong>Windows Vista и Windows Server 2008:</strong> Это значение не поддерживается до Windows 7 и Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="2a693-150"><strong>Windows Vista and Windows Server 2008:</strong> This value is not supported until Windows 7 and Windows Server 2008 R2.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a693-151">ресаурцебасе</span><span class="sxs-lookup"><span data-stu-id="2a693-151">resourceBase</span></span></td>
<td><span data-ttu-id="2a693-152"><a href="performance-counters-uint32type-simple-type.md"><strong>мужчина: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a693-152"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><p><span data-ttu-id="2a693-153">Определяет начальное значение индекса ресурса, которое <a href="ctrpp.md">КТРПП</a> использует для создания идентификаторов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a693-153">Defines the starting resource index value that <a href="ctrpp.md">CTRPP</a> uses to generate the resource identifiers.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a693-154">символ</span><span class="sxs-lookup"><span data-stu-id="2a693-154">symbol</span></span></td>
<td><span data-ttu-id="2a693-155"><a href="performance-counters-csymboltype-simple-type.md"><strong>мужчина: Ксимболтипе</strong></a></span><span class="sxs-lookup"><span data-stu-id="2a693-155"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><p><span data-ttu-id="2a693-156">Символьное имя, идентифицирующее поставщик.</span><span class="sxs-lookup"><span data-stu-id="2a693-156">A symbolic name that identifies the provider.</span></span> <span data-ttu-id="2a693-157">Средство <a href="ctrpp.md">КТРПП</a> создает переменную Handle, которую можно использовать при вызове функций, которым требуется маркер поставщика (например, <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>перфсетулонгкаунтервалуе</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="2a693-157">The <a href="ctrpp.md">CTRPP</a> tool creates a HANDLE variable that you can use when calling functions that require a handle to the provider (for example, <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>PerfSetULongCounterValue</strong></a>).</span></span> <span data-ttu-id="2a693-158">Символическое имя — это имя переменной.</span><span class="sxs-lookup"><span data-stu-id="2a693-158">The symbolic name is the name of the variable.</span></span></p>
<p><span data-ttu-id="2a693-159">При включении аргумента <strong>-prefix</strong> при вызове <a href="ctrpp.md">КТРПП</a>Строка префикса добавляется в начало символьного имени.</span><span class="sxs-lookup"><span data-stu-id="2a693-159">If you include the <strong>-prefix</strong> argument when calling <a href="ctrpp.md">CTRPP</a>, the prefix string is added to the beginning of the symbolic name.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="2a693-160">Требования</span><span class="sxs-lookup"><span data-stu-id="2a693-160">Requirements</span></span>



| <span data-ttu-id="2a693-161">Требование</span><span class="sxs-lookup"><span data-stu-id="2a693-161">Requirement</span></span> | <span data-ttu-id="2a693-162">Значение</span><span class="sxs-lookup"><span data-stu-id="2a693-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2a693-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a693-163">Minimum supported client</span></span><br/> | <span data-ttu-id="2a693-164">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a693-164">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2a693-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a693-165">Minimum supported server</span></span><br/> | <span data-ttu-id="2a693-166">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2a693-166">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




