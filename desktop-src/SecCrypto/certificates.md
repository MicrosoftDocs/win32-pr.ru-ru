---
description: Представляет коллекцию объектов Certificate.
ms.assetid: 82011c49-38fb-4261-8fb3-b76859da8a9e
title: Объект Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e8c12c16820342c5687720a35ce81aa7b94f180
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665043"
---
# <a name="certificates-object"></a><span data-ttu-id="cd9d4-103">Объект Certificates</span><span class="sxs-lookup"><span data-stu-id="cd9d4-103">Certificates object</span></span>

<span data-ttu-id="cd9d4-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="cd9d4-105">Вместо этого используйте [**класс X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="cd9d4-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="cd9d4-106">Объект **Certificates** представляет коллекцию объектов [**Certificate**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="cd9d4-106">The **Certificates** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="cd9d4-107">Каждый объект [**сертификата**](certificate.md) представляет один [*цифровой сертификат*](../secgloss/d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cd9d4-107">Each [**Certificate**](certificate.md) object represents a single [*digital certificate*](../secgloss/d-gly.md).</span></span>

<span data-ttu-id="cd9d4-108">Объект **Certificates** предоставляет следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="cd9d4-108">The **Certificates** object exposes the following interfaces:</span></span>

-   <span data-ttu-id="cd9d4-109">**ICertificates2**: представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-109">**ICertificates2**: Introduced in CAPICOM 2.0.</span></span>
-   <span data-ttu-id="cd9d4-110">**Ицертификатес**: представлено в CAPICOM 1,0.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-110">**ICertificates**: Introduced in CAPICOM 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="cd9d4-111">Назначение</span><span class="sxs-lookup"><span data-stu-id="cd9d4-111">When to use</span></span>

<span data-ttu-id="cd9d4-112">Объект **Certificates** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="cd9d4-112">The **Certificates** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="cd9d4-113">Добавление или удаление объекта [**сертификата**](certificate.md) в коллекции или из нее.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-113">Add or remove a [**Certificate**](certificate.md) object to or from the collection.</span></span>
-   <span data-ttu-id="cd9d4-114">Создание подмножества коллекции путем поиска набора сертификатов или отображения диалогового окна для выбора сертификатов.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-114">Generate a subset of the collection by finding a set of certificates or by displaying a dialog box to select the certificates.</span></span>
-   <span data-ttu-id="cd9d4-115">Очистить все объекты [**сертификата**](certificate.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-115">Clear all the [**Certificate**](certificate.md) objects from the collection.</span></span>
-   <span data-ttu-id="cd9d4-116">Получение числа сертификатов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-116">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="cd9d4-117">Получение конкретного объекта [**сертификата**](certificate.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-117">Retrieve a specific [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="cd9d4-118">Выполните итерацию по коллекции.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-118">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="cd9d4-119">Элементы</span><span class="sxs-lookup"><span data-stu-id="cd9d4-119">Members</span></span>

<span data-ttu-id="cd9d4-120">Объект **Certificates** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cd9d4-120">The **Certificates** object has these types of members:</span></span>

-   [<span data-ttu-id="cd9d4-121">Методы</span><span class="sxs-lookup"><span data-stu-id="cd9d4-121">Methods</span></span>](#methods)
-   [<span data-ttu-id="cd9d4-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="cd9d4-122">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cd9d4-123">Методы</span><span class="sxs-lookup"><span data-stu-id="cd9d4-123">Methods</span></span>

<span data-ttu-id="cd9d4-124">Объект **Certificates** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-124">The **Certificates** object has these methods.</span></span>



| <span data-ttu-id="cd9d4-125">Метод</span><span class="sxs-lookup"><span data-stu-id="cd9d4-125">Method</span></span>                                | <span data-ttu-id="cd9d4-126">Описание</span><span class="sxs-lookup"><span data-stu-id="cd9d4-126">Description</span></span>                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd9d4-127">**Включить**</span><span class="sxs-lookup"><span data-stu-id="cd9d4-127">**Add**</span></span>](certificates-add.md)       | <span data-ttu-id="cd9d4-128">Добавляет объект [**сертификата**](certificate.md) в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-128">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/> <span data-ttu-id="cd9d4-129">(Наследуется от **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="cd9d4-129">(Inherited from **CertificatesICertificates2**)</span></span>                                        |
| [<span data-ttu-id="cd9d4-130">**Открытым**</span><span class="sxs-lookup"><span data-stu-id="cd9d4-130">**Clear**</span></span>](certificates-clear.md)   | <span data-ttu-id="cd9d4-131">Удаляет все объекты [**сертификата**](certificate.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-131">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> <span data-ttu-id="cd9d4-132">(Наследуется от **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="cd9d4-132">(Inherited from **CertificatesICertificates2**)</span></span>                                |
| [<span data-ttu-id="cd9d4-133">**Поиск**</span><span class="sxs-lookup"><span data-stu-id="cd9d4-133">**Find**</span></span>](certificates-find.md)     | <span data-ttu-id="cd9d4-134">Возвращает объект **Certificates** , который содержит все сертификаты, соответствующие указанным условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-134">Returns a **Certificates** object that contains all certificates that match the specified search criteria.</span></span><br/> <span data-ttu-id="cd9d4-135">(Наследуется от **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="cd9d4-135">(Inherited from **CertificatesICertificates2**)</span></span> |
| [<span data-ttu-id="cd9d4-136">**Отменит**</span><span class="sxs-lookup"><span data-stu-id="cd9d4-136">**Remove**</span></span>](certificates-remove.md) | <span data-ttu-id="cd9d4-137">Удаляет из коллекции один объект [**сертификата**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="cd9d4-137">Removes a single [**Certificate**](certificate.md) object from the collection.</span></span><br/> <span data-ttu-id="cd9d4-138">(Наследуется от **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="cd9d4-138">(Inherited from **CertificatesICertificates2**)</span></span>                            |
| [<span data-ttu-id="cd9d4-139">**Сохранить**</span><span class="sxs-lookup"><span data-stu-id="cd9d4-139">**Save**</span></span>](certificates-save.md)     | <span data-ttu-id="cd9d4-140">Сохраняет сертификаты в указанный файл.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-140">Saves the certificates to a specified file.</span></span><br/> <span data-ttu-id="cd9d4-141">(Наследуется от **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="cd9d4-141">(Inherited from **CertificatesICertificates2**)</span></span>                                                                |
| [<span data-ttu-id="cd9d4-142">**Метьте**</span><span class="sxs-lookup"><span data-stu-id="cd9d4-142">**Select**</span></span>](certificates-select.md) | <span data-ttu-id="cd9d4-143">Отображает диалоговое окно для выбора сертификатов и возвращает коллекцию выбранных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-143">Displays a dialog box for selecting certificates and returns a collection of those certificates selected.</span></span><br/> <span data-ttu-id="cd9d4-144">(Наследуется от **CertificatesICertificates2**)</span><span class="sxs-lookup"><span data-stu-id="cd9d4-144">(Inherited from **CertificatesICertificates2**)</span></span>  |



 

### <a name="properties"></a><span data-ttu-id="cd9d4-145">Свойства</span><span class="sxs-lookup"><span data-stu-id="cd9d4-145">Properties</span></span>

<span data-ttu-id="cd9d4-146">Объект **Certificates** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-146">The **Certificates** object has these properties.</span></span>



| <span data-ttu-id="cd9d4-147">Свойство</span><span class="sxs-lookup"><span data-stu-id="cd9d4-147">Property</span></span>                                             | <span data-ttu-id="cd9d4-148">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="cd9d4-148">Access type</span></span>          | <span data-ttu-id="cd9d4-149">Описание</span><span class="sxs-lookup"><span data-stu-id="cd9d4-149">Description</span></span>                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd9d4-150">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="cd9d4-150">**\_NewEnum**</span></span>](certificates-newenum.md)<br/> | <span data-ttu-id="cd9d4-151">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd9d4-151">Read-only</span></span><br/> | <span data-ttu-id="cd9d4-152">Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который может быть использован для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-152">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="cd9d4-153">Это свойство скрыто в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="cd9d4-153">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="cd9d4-154">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="cd9d4-154">**Count**</span></span>](certificates-count.md)<br/>       | <span data-ttu-id="cd9d4-155">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd9d4-155">Read-only</span></span><br/> | <span data-ttu-id="cd9d4-156">Возвращает количество объектов [**сертификата**](certificate.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-156">Retrieves the number of [**Certificate**](certificate.md) objects in the collection.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="cd9d4-157">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="cd9d4-157">**Item**</span></span>](certificates-item.md)<br/>         | <span data-ttu-id="cd9d4-158">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd9d4-158">Read-only</span></span><br/> | <span data-ttu-id="cd9d4-159">Извлекает объект [**сертификата**](certificate.md) , представляющий индексированный сертификат коллекции.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-159">Retrieves a [**Certificate**](certificate.md) object that represents the indexed certificate of the collection.</span></span> <span data-ttu-id="cd9d4-160">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-160">This is the default property.</span></span><br/> <span data-ttu-id="cd9d4-161">(Наследуется от **CertificatesICertificates2ICertificates**)</span><span class="sxs-lookup"><span data-stu-id="cd9d4-161">(Inherited from **CertificatesICertificates2ICertificates**)</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="cd9d4-162">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd9d4-162">Remarks</span></span>

<span data-ttu-id="cd9d4-163">Объект **Certificates** может быть создан и защищен для создания скриптов.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-163">The **Certificates** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="cd9d4-164">ProgID для объекта **Certificates** — CAPICOM. Certificates. 2.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-164">The ProgID for the **Certificates** object is "CAPICOM.Certificates.2".</span></span>

<span data-ttu-id="cd9d4-165">**CAPICOM 1. *x*:** ProgID для объекта **Certificates** — CAPICOM. Certificates. 1.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-165">**CAPICOM 1.*x*:** The ProgID for the **Certificates** object is "CAPICOM.Certificates.1".</span></span>

## <a name="requirements"></a><span data-ttu-id="cd9d4-166">Требования</span><span class="sxs-lookup"><span data-stu-id="cd9d4-166">Requirements</span></span>



| <span data-ttu-id="cd9d4-167">Требование</span><span class="sxs-lookup"><span data-stu-id="cd9d4-167">Requirement</span></span> | <span data-ttu-id="cd9d4-168">Значение</span><span class="sxs-lookup"><span data-stu-id="cd9d4-168">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd9d4-169">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="cd9d4-169">End of client support</span></span><br/> | <span data-ttu-id="cd9d4-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd9d4-170">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cd9d4-171">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="cd9d4-171">End of server support</span></span><br/> | <span data-ttu-id="cd9d4-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd9d4-172">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cd9d4-173">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="cd9d4-173">Redistributable</span></span><br/>       | <span data-ttu-id="cd9d4-174">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="cd9d4-174">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cd9d4-175">DLL</span><span class="sxs-lookup"><span data-stu-id="cd9d4-175">DLL</span></span><br/>                   | <dl> <span data-ttu-id="cd9d4-176"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd9d4-176"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd9d4-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd9d4-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd9d4-178">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="cd9d4-178">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
