---
description: Обертка поставщика заключается в том, чтобы инкапсулировать и использовать низкоуровневые интерфейсы COM (предоставляемые производителями смарт-карт) для конкретной смарт-карты. Эти интерфейсы не предоставляются корпорацией Майкрософт.
ms.assetid: 7bc26f7b-c355-448a-9f23-4ccfffea2fef
title: Поставщик службы-оболочки поставщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b7d22fea8e450111e1611f2ec069697c229a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144635"
---
# <a name="vendor-wrapper-service-provider"></a><span data-ttu-id="e4039-104">Поставщик службы-оболочки поставщика</span><span class="sxs-lookup"><span data-stu-id="e4039-104">Vendor Wrapper Service Provider</span></span>

<span data-ttu-id="e4039-105">Обертка поставщика заключается в том, чтобы инкапсулировать и использовать низкоуровневые интерфейсы COM (предоставляемые производителями смарт-карт) для конкретной смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="e4039-105">The purpose of the vendor wrapper is to encapsulate and use the low-level COM interfaces (supplied by the smart card manufacturers) for a particular smart card.</span></span> <span data-ttu-id="e4039-106">Эти интерфейсы не предоставляются корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="e4039-106">These interfaces are not supplied by Microsoft.</span></span>

![оболочка поставщика](images/scspart1.png)

<span data-ttu-id="e4039-108">Как описано в части 6 *спецификации взаимодействия для систем Иккс и персональных компьютеров* (см. спецификации в [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ), функциональные возможности, предоставляемые этой оболочкой, проще в использовании, чем у четырех отдельных поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="e4039-108">As described in part 6 of the *Interoperability Specification for ICCs and Personal Computer Systems* (see specifications at [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/)), the functionality exposed by this wrapper is easier to use than the functionality of four separate service providers.</span></span> <span data-ttu-id="e4039-109">Функциональные возможности оболочки можно разделить на четыре основные области:</span><span class="sxs-lookup"><span data-stu-id="e4039-109">The wrapper's functionality can be divided into four main areas:</span></span>

-   <span data-ttu-id="e4039-110">Службы проверки подлинности смарт-карт, такие как получение запроса и проверка подлинности карты.</span><span class="sxs-lookup"><span data-stu-id="e4039-110">Smart card authentication services, such as get challenge and card authentication.</span></span>
-   <span data-ttu-id="e4039-111">Доступ к файлу смарт-карты или службы файловой системы, такие как открытие, закрытие, чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="e4039-111">Smart card file access or file system services, such as open, close, read, and write.</span></span>
-   <span data-ttu-id="e4039-112">Управление смарт-картами, например подключение и отсоединение.</span><span class="sxs-lookup"><span data-stu-id="e4039-112">Smart card management, such as attach and detach.</span></span>
-   <span data-ttu-id="e4039-113">Службы проверки смарт-карт, такие как проверка и изменение кода.</span><span class="sxs-lookup"><span data-stu-id="e4039-113">Smart card verification services, such as verify and change code.</span></span>

> [!Note]  
> <span data-ttu-id="e4039-114">Эта спецификация может быть недоступна в некоторых языках и странах или регионах.</span><span class="sxs-lookup"><span data-stu-id="e4039-114">This specification may not be available in some languages and countries or regions.</span></span>

 

<span data-ttu-id="e4039-115">Функциональные возможности зависят от типа используемой карты (функции, поддерживаемые картой, протоколы и т. д.) и будут отличаться для каждой карты.</span><span class="sxs-lookup"><span data-stu-id="e4039-115">The functionality is specific to the type of card being used (which functions the card supports, protocols, and so on) and will be different for each card.</span></span>

<span data-ttu-id="e4039-116">Пример оболочки Microsoft Скардком использует библиотеку ATL COM для реализации простой оболочки и размещения шаблона для других оболочек.</span><span class="sxs-lookup"><span data-stu-id="e4039-116">The Microsoft SCardCOM example wrapper uses the ATL COM library to implement a simple wrapper and lay down a template for other wrappers.</span></span> <span data-ttu-id="e4039-117">Он реализует следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="e4039-117">It implements the following interfaces.</span></span>



| <span data-ttu-id="e4039-118">Интерфейс или объект</span><span class="sxs-lookup"><span data-stu-id="e4039-118">Interface or object</span></span>                                     | <span data-ttu-id="e4039-119">Описание</span><span class="sxs-lookup"><span data-stu-id="e4039-119">Description</span></span>                         |
|---------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="e4039-120">**искардаус**</span><span class="sxs-lookup"><span data-stu-id="e4039-120">**ISCardAuth**</span></span>](iscardauth.md)<br/>             | <span data-ttu-id="e4039-121">Службы проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e4039-121">Authentication services.</span></span><br/> |
| [<span data-ttu-id="e4039-122">**искардфилеакцесс**</span><span class="sxs-lookup"><span data-stu-id="e4039-122">**ISCardFileAccess**</span></span>](iscardfileaccess.md)<br/> | <span data-ttu-id="e4039-123">Службы файловой системы.</span><span class="sxs-lookup"><span data-stu-id="e4039-123">File system services.</span></span><br/>    |
| [<span data-ttu-id="e4039-124">**искардманаже**</span><span class="sxs-lookup"><span data-stu-id="e4039-124">**ISCardManage**</span></span>](iscardmanage.md)<br/>         | <span data-ttu-id="e4039-125">Службы управления.</span><span class="sxs-lookup"><span data-stu-id="e4039-125">Management services.</span></span><br/>     |
| [<span data-ttu-id="e4039-126">**искардверифи**</span><span class="sxs-lookup"><span data-stu-id="e4039-126">**ISCardVerify**</span></span>](iscardverify.md)<br/>         | <span data-ttu-id="e4039-127">Службы проверки.</span><span class="sxs-lookup"><span data-stu-id="e4039-127">Verification services.</span></span><br/>   |



 

> [!Note]  
> <span data-ttu-id="e4039-128">Пример Скардком предоставляется только в качестве примера реализации интерфейсов-оболочек.</span><span class="sxs-lookup"><span data-stu-id="e4039-128">The SCardCOM example is provided only as an example of implementing the wrapper interfaces.</span></span> <span data-ttu-id="e4039-129">Чтобы предотвратить конфликт имен DLL с другими поставщиками, не следует использовать SCardCOM.dll в качестве имени создаваемых библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="e4039-129">To prevent DLL name collision with other vendors, you must not use SCardCOM.dll as the name of any DLLs you create.</span></span>

 

<span data-ttu-id="e4039-130">Ниже приведен типичный пример использования оболочки поставщика.</span><span class="sxs-lookup"><span data-stu-id="e4039-130">Following is a typical use of the vendor wrapper.</span></span> <span data-ttu-id="e4039-131">В этом примере используется интерфейс [**искардманаже**](iscardmanage.md) для создания экземпляров интерфейсов, которые будут инкапсулированы в поставщик службы, и интерфейс [**искардверифи**](iscardverify.md) для проверки их работы.</span><span class="sxs-lookup"><span data-stu-id="e4039-131">This example uses the [**ISCardManage**](iscardmanage.md) interface to create instances of the interfaces that will be wrapped into the service provider and the [**ISCardVerify**](iscardverify.md) interface to verify their operation.</span></span>

<span data-ttu-id="e4039-132">**Создание поставщика службы-оболочки**</span><span class="sxs-lookup"><span data-stu-id="e4039-132">**To build a wrapper service provider**</span></span>

1.  <span data-ttu-id="e4039-133">Создайте экземпляр интерфейса [**искардманаже**](iscardmanage.md) .</span><span class="sxs-lookup"><span data-stu-id="e4039-133">Create an instance of the [**ISCardManage**](iscardmanage.md) interface.</span></span> <span data-ttu-id="e4039-134">Используйте этот интерфейс для создания экземпляра требуемых интерфейсов (например, [**искардфилеакцесс**](iscardfileaccess.md) или [**искардверифи**](iscardverify.md)).</span><span class="sxs-lookup"><span data-stu-id="e4039-134">Use this interface to create an instance of required interfaces (for example, [**ISCardFileAccess**](iscardfileaccess.md) or [**ISCardVerify**](iscardverify.md)).</span></span> <span data-ttu-id="e4039-135">При создании этих интерфейсов также создаются все соответствующие COM-интерфейсы низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="e4039-135">When creating these interfaces, any corresponding low-level COM interfaces would also be created.</span></span>
2.  <span data-ttu-id="e4039-136">Подключите или подключитесь к карте с помощью соответствующего метода [**искардманаже**](iscardmanage.md) .</span><span class="sxs-lookup"><span data-stu-id="e4039-136">Attach/connect to a card through the appropriate [**ISCardManage**](iscardmanage.md) method.</span></span>
3.  <span data-ttu-id="e4039-137">Выполните необходимые операции с помощью соответствующего метода [**искардверифи**](iscardverify.md) (который может вызывать несколько низкоуровневых COM-интерфейсов и методов для завершения).</span><span class="sxs-lookup"><span data-stu-id="e4039-137">Perform required operations through the appropriate [**ISCardVerify**](iscardverify.md) method (which may call multiple low-level COM interfaces and methods to complete).</span></span>
4.  <span data-ttu-id="e4039-138">Повторите операцию для других операций.</span><span class="sxs-lookup"><span data-stu-id="e4039-138">Repeat for other operations.</span></span>
5.  <span data-ttu-id="e4039-139">Выпуск по завершении.</span><span class="sxs-lookup"><span data-stu-id="e4039-139">Release when complete.</span></span>

<span data-ttu-id="e4039-140">Имя COM-интерфейса и идентификатор интерфейса (GUID) не должны изменяться из тех, которые используются в коде или образце оболочки.</span><span class="sxs-lookup"><span data-stu-id="e4039-140">The COM interface name and interface identifier (GUID) should not change from those used in the code or example wrapper.</span></span> <span data-ttu-id="e4039-141">Однако идентификатор GUID класса (то есть, где находится фактическая реализация интерфейса) должен быть изменен из используемых.</span><span class="sxs-lookup"><span data-stu-id="e4039-141">However, the class GUID (that is, where an actual implementation of an interface resides) must be changed from those used.</span></span> <span data-ttu-id="e4039-142">Это особенно важно при реализации оболочки поставщика.</span><span class="sxs-lookup"><span data-stu-id="e4039-142">This is especially important when implementing a vendor wrapper.</span></span> <span data-ttu-id="e4039-143">Одним из примеров может быть использование нескольких оболочек поставщика на определенном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e4039-143">One example would be using multiple vendor wrappers on a particular computer.</span></span> <span data-ttu-id="e4039-144">Эти оболочки должны реализовывать одни и те же COM-интерфейсы, но всегда будут использовать разные стратегии реализации.</span><span class="sxs-lookup"><span data-stu-id="e4039-144">These wrappers should implement the same COM interfaces, but will always use different implementation strategies.</span></span> <span data-ttu-id="e4039-145">Поэтому требуются разные классы (и идентификаторы классов).</span><span class="sxs-lookup"><span data-stu-id="e4039-145">Therefore, different classes (and class IDs) are required.</span></span>

 

 




