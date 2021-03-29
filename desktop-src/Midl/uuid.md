---
title: uuid - атрибут
description: Атрибут интерфейса \ UUID \ определяет универсальный уникальный идентификатор (UUID), назначенный интерфейсу, который отличает его от других интерфейсов.
ms.assetid: 72cf12f5-49cd-440d-9665-73211509d050
keywords:
- атрибут UUID MIDL
topic_type:
- apiref
api_name:
- uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5688bafe8343bdc1ab508a4e65984cc15c88b124
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784071"
---
# <a name="uuid-attribute"></a><span data-ttu-id="2390e-104">uuid - атрибут</span><span class="sxs-lookup"><span data-stu-id="2390e-104">uuid attribute</span></span>

<span data-ttu-id="2390e-105">Атрибут интерфейса **\[ UUID \]** обозначает универсальный уникальный идентификатор (UUID), назначенный интерфейсу, который отличает его от других интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="2390e-105">The **\[uuid\]** interface attribute designates a universally unique identifier (UUID) that is assigned to the interface and that distinguishes it from other interfaces.</span></span>

``` syntax
uuid (string-uuid) 
uuid ("string-uuid")
```

## <a name="parameters"></a><span data-ttu-id="2390e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2390e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2390e-107">*Строка UUID*</span><span class="sxs-lookup"><span data-stu-id="2390e-107">*string-uuid*</span></span> 
</dt> <dd>

<span data-ttu-id="2390e-108">Задает строку, состоящую из 8 шестнадцатеричных цифр, за которыми следует дефис, затем три группы из четырех шестнадцатеричных цифр, за которыми следует дефис, а затем 12 шестнадцатеричных цифр.</span><span class="sxs-lookup"><span data-stu-id="2390e-108">Specifies a string consisting of 8 hexadecimal digits followed by a hyphen, then three groups of 4 hexadecimal digits each followed by a hyphen, then 12 hexadecimal digits.</span></span> <span data-ttu-id="2390e-109">Строку UUID можно заключать в кавычки, за исключением случаев, когда используется параметр компилятора MIDL [**/ОСФ**](-osf.md).</span><span class="sxs-lookup"><span data-stu-id="2390e-109">You can enclose the UUID string in quotes, except when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2390e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2390e-110">Remarks</span></span>

<span data-ttu-id="2390e-111">Библиотека времени выполнения использует UUID интерфейса, который указывает атрибут **\[ UUID \]** , чтобы обеспечить взаимодействие между клиентскими и серверными приложениями.</span><span class="sxs-lookup"><span data-stu-id="2390e-111">The run-time library uses the interface UUID that the **\[uuid\]** attribute designates to help establish communication between the client and server applications.</span></span> <span data-ttu-id="2390e-112">Атрибут **\[ UUID \]** может присутствовать в списке атрибутов интерфейса либо для интерфейса RPC, либо для COM-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2390e-112">The **\[uuid\]** attribute can appear in the interface attribute list for either an RPC interface or a COM interface.</span></span>

<span data-ttu-id="2390e-113">Для интерфейса RPC список атрибутов интерфейса должен содержать либо атрибут **\[ UUID \]** , либо **\[** [**локальный**](local.md) **\]** атрибут, и выбранный вариант должен быть ровно один раз.</span><span class="sxs-lookup"><span data-stu-id="2390e-113">For an RPC interface, the interface attribute list must include either the **\[uuid\]** attribute or the **\[**[**local**](local.md)**\]** attribute, and the one you choose must occur exactly once.</span></span> <span data-ttu-id="2390e-114">Если список содержит атрибут **\[ UUID \]** , он также может включать **\[** атрибут [**Version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="2390e-114">If the list includes the **\[uuid\]** attribute, it can also include the **\[**[**version**](version.md)**\]** attribute.</span></span>

<span data-ttu-id="2390e-115">Для COM-интерфейса (определяемого **\[** [](object.md) **\]** атрибутом интерфейса объектов) список атрибутов интерфейса должен включать атрибут **\[ UUID \]** , но не может включать атрибут **\[ Version \]** .</span><span class="sxs-lookup"><span data-stu-id="2390e-115">For a COM interface (identified by the **\[**[**object**](object.md)**\]** interface attribute), the interface attribute list must include the **\[uuid\]** attribute, but it cannot include the **\[version\]** attribute.</span></span> <span data-ttu-id="2390e-116">Список для COM-интерфейса может включать **\[ локальный \]** атрибут, даже если имеется атрибут **\[ UUID \]** .</span><span class="sxs-lookup"><span data-stu-id="2390e-116">The list for a COM interface can include the **\[local\]** attribute even though the **\[uuid\]** attribute is present.</span></span>

<span data-ttu-id="2390e-117">Microsoft RPC поддерживает расширение для устройства DCE IDL, позволяющее заключать UUID в двойные кавычки ("" ").</span><span class="sxs-lookup"><span data-stu-id="2390e-117">Microsoft RPC supports an extension to DCE IDL that allows the UUID to be enclosed in double quotation marks ("" "").</span></span> <span data-ttu-id="2390e-118">Форма в кавычках необходима для препроцессоров C-компилятора, которые преобразуют числа UUID в виде чисел с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="2390e-118">The quoted form is needed for C-compiler preprocessors that interpret UUID numbers as floating-point numbers.</span></span>

<span data-ttu-id="2390e-119">Для обеспечения уникальности все значения UUID должны быть сформированы компьютером.</span><span class="sxs-lookup"><span data-stu-id="2390e-119">All UUID values should be computer-generated to guarantee uniqueness.</span></span> <span data-ttu-id="2390e-120">Используйте служебную программу uuidgen для создания уникальных значений UUID.</span><span class="sxs-lookup"><span data-stu-id="2390e-120">Use the Uuidgen utility to generate unique UUID values.</span></span>

<span data-ttu-id="2390e-121">Идентификатор UUID и номер версии интерфейса используются для определения возможности привязки клиента к серверу.</span><span class="sxs-lookup"><span data-stu-id="2390e-121">The UUID and version numbers of the interface are used to determine whether the client can bind to the server.</span></span> <span data-ttu-id="2390e-122">Для привязки клиента к серверу UUID, указанный в интерфейсах клиента и сервера, должен быть одинаковым.</span><span class="sxs-lookup"><span data-stu-id="2390e-122">For the client to bind to the server, the UUID specified in the client and server interfaces must be the same.</span></span>

<span data-ttu-id="2390e-123">Обратите внимание, что интерфейс без атрибутов можно импортировать в базовый IDL-файл.</span><span class="sxs-lookup"><span data-stu-id="2390e-123">Note that an interface without attributes can be imported into a base IDL file.</span></span> <span data-ttu-id="2390e-124">Однако интерфейс должен содержать только типы данными без процедур.</span><span class="sxs-lookup"><span data-stu-id="2390e-124">However, the interface must contain only datatypes with no procedures.</span></span> <span data-ttu-id="2390e-125">Если в интерфейсе содержится даже одна процедура, необходимо указать локальный или UUID.</span><span class="sxs-lookup"><span data-stu-id="2390e-125">If even one procedure is contained in the interface, a local or UUID attribute must be specified.</span></span>

## <a name="examples"></a><span data-ttu-id="2390e-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="2390e-126">Examples</span></span>

``` syntax
uuid(6B29FC40-CA47-1067-B31D-00DD010662DA) 
 
uuid("6B29FC40-CA47-1067-B31D-00DD010662DA")
```

## <a name="see-also"></a><span data-ttu-id="2390e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2390e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2390e-128">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="2390e-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="2390e-129">**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="2390e-129">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="2390e-130">**Языковые**</span><span class="sxs-lookup"><span data-stu-id="2390e-130">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="2390e-131">**объектами**</span><span class="sxs-lookup"><span data-stu-id="2390e-131">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="2390e-132">**/осф**</span><span class="sxs-lookup"><span data-stu-id="2390e-132">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="2390e-133">**Версия**</span><span class="sxs-lookup"><span data-stu-id="2390e-133">**version**</span></span>](version.md)
</dt> </dl>

 

 




