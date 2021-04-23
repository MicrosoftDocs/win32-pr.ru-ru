---
description: Определяет коды ошибок, возвращаемые CAPICOM.
ms.assetid: e72b8290-b482-4629-8b87-5a15677865a6
title: Перечисление CAPICOM_ERROR_CODE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ERROR_CODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: ccd4963c83f1ad7ce3bc686b7736ce47d699ce30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668714"
---
# <a name="capicom_error_code-enumeration"></a><span data-ttu-id="74c16-103">\_ \_ Перечисление кода ошибки CAPICOM</span><span class="sxs-lookup"><span data-stu-id="74c16-103">CAPICOM\_ERROR\_CODE enumeration</span></span>

<span data-ttu-id="74c16-104">Тип перечисления " **CAPICOM \_ \_ Code Error** " определяет коды ошибок, возвращаемые CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="74c16-104">The **CAPICOM\_ERROR\_CODE** enumeration type defines error codes that are returned by CAPICOM.</span></span>

> [!Note]  
> <span data-ttu-id="74c16-105">Visual Basic ошибки выпуска сценариев возвращают значение **Err. Number** больше нуля.</span><span class="sxs-lookup"><span data-stu-id="74c16-105">Visual Basic Scripting Edition errors return an **Err.number** value greater than zero.</span></span> <span data-ttu-id="74c16-106">Для этих ошибок значения **Err. Description** содержат сведения о причине ошибки.</span><span class="sxs-lookup"><span data-stu-id="74c16-106">For those errors, **Err.Description** values provide information about the cause of the error.</span></span> <span data-ttu-id="74c16-107">Помимо Visual Basic ошибок выпуска сценариев, CAPICOM Errors возвращает коды, определенные **\_ \_ кодом ошибки CAPICOM**.</span><span class="sxs-lookup"><span data-stu-id="74c16-107">In addition to Visual Basic Scripting Edition errors, CAPICOM errors return the codes defined by **CAPICOM\_ERROR\_CODE**.</span></span>

 

## <a name="members"></a><span data-ttu-id="74c16-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="74c16-108">Members</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="74c16-109">Член</span><span class="sxs-lookup"><span data-stu-id="74c16-109">Member</span></span></th>
<th><span data-ttu-id="74c16-110">Описание</span><span class="sxs-lookup"><span data-stu-id="74c16-110">Description</span></span></th>
<th><span data-ttu-id="74c16-111">Значение</span><span class="sxs-lookup"><span data-stu-id="74c16-111">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="74c16-112"><strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-112"><strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="74c16-113">Использован недопустимый тип кодирования.</span><span class="sxs-lookup"><span data-stu-id="74c16-113">An encoding type that is not valid was used.</span></span><br/> <span data-ttu-id="74c16-114">В следующем списке приведены допустимые типы кодировки.</span><span class="sxs-lookup"><span data-stu-id="74c16-114">The following list shows the valid encoding types:</span></span>
<ul>
<li><span data-ttu-id="74c16-115">CAPICOM_ENCODE_ANY</span><span class="sxs-lookup"><span data-stu-id="74c16-115">CAPICOM_ENCODE_ANY</span></span></li>
<li><span data-ttu-id="74c16-116">CAPICOM_ENCODE_BASE64</span><span class="sxs-lookup"><span data-stu-id="74c16-116">CAPICOM_ENCODE_BASE64</span></span></li>
<li><span data-ttu-id="74c16-117">CAPICOM_ENCODE_BINARY</span><span class="sxs-lookup"><span data-stu-id="74c16-117">CAPICOM_ENCODE_BINARY</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="74c16-118">0x80880100</span><span class="sxs-lookup"><span data-stu-id="74c16-118">0x80880100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-119"><strong>CAPICOM_E_EKU_INVALID_OID</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-119"><strong>CAPICOM_E_EKU_INVALID_OID</strong></span></span></td>
<td><span data-ttu-id="74c16-120">Свойство <a href="eku-oid.md"><strong>OID</strong></a> объекта <a href="eku.md"><strong>EKU</strong></a> не может быть задано, так как свойство <a href="eku-name.md"><strong>Name</strong></a> не имеет значение CAPICOM_EKU_OTHER.</span><span class="sxs-lookup"><span data-stu-id="74c16-120">The <a href="eku-oid.md"><strong>OID</strong></a> property of the <a href="eku.md"><strong>EKU</strong></a> object cannot be set because the <a href="eku-name.md"><strong>Name</strong></a> property is not set to CAPICOM_EKU_OTHER.</span></span><br/> <span data-ttu-id="74c16-121">Присвойте свойству <a href="eku-name.md"><strong>Name</strong></a> значение CAPICOM_EKU_OTHER, прежде чем задавать свойство <a href="eku-oid.md"><strong>OID</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-121">Set the <a href="eku-name.md"><strong>Name</strong></a> property to CAPICOM_EKU_OTHER before setting the <a href="eku-oid.md"><strong>OID</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="74c16-122">0x80880200</span><span class="sxs-lookup"><span data-stu-id="74c16-122">0x80880200</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-123"><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-123"><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="74c16-124">Свойство <a href="eku-oid.md"><strong>OID</strong></a> объекта <a href="eku.md"><strong>EKU</strong></a> не инициализировано.</span><span class="sxs-lookup"><span data-stu-id="74c16-124">The <a href="eku-oid.md"><strong>OID</strong></a> property of the <a href="eku.md"><strong>EKU</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="74c16-125">Либо задайте для свойства <a href="eku-name.md"><strong>Name</strong></a> значение, отличное от CAPICOM_EKU_OTHER, либо установите свойство <strong>Name</strong> в CAPICOM_EKU_OTHER и свойство <a href="eku-oid.md"><strong>OID</strong></a> в качестве значения.</span><span class="sxs-lookup"><span data-stu-id="74c16-125">Either set the <a href="eku-name.md"><strong>Name</strong></a> property to anything other than CAPICOM_EKU_OTHER, or set the <strong>Name</strong> property to CAPICOM_EKU_OTHER and the <a href="eku-oid.md"><strong>OID</strong></a> property to a value.</span></span><br/></td>
<td><span data-ttu-id="74c16-126">0x80880201</span><span class="sxs-lookup"><span data-stu-id="74c16-126">0x80880201</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-127"><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-127"><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="74c16-128">Объект <a href="certificate.md"><strong>сертификата</strong></a> не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="74c16-128">The <a href="certificate.md"><strong>Certificate</strong></a> object has not been initialized.</span></span><br/> <span data-ttu-id="74c16-129">Как правило, этот код ошибки возвращается, когда экземпляр объекта <a href="certificate.md"><strong>сертификата</strong></a> создается, но не связан с цифровым сертификатом.</span><span class="sxs-lookup"><span data-stu-id="74c16-129">Usually, this error code is returned when a <a href="certificate.md"><strong>Certificate</strong></a> object is instantiated but not associated with a digital certificate.</span></span> <span data-ttu-id="74c16-130">Чтобы связать объект с цифровым сертификатом, либо назначьте его существующему объекту <strong>сертификата</strong> , либо вызовите метод <a href="certificate-import.md"><strong>Import</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-130">To associate the object with a digital certificate, either assign it to an existing <strong>Certificate</strong> object or call the <a href="certificate-import.md"><strong>Import</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="74c16-131">0x80880210</span><span class="sxs-lookup"><span data-stu-id="74c16-131">0x80880210</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-132"><strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-132"><strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong></span></span></td>
<td><span data-ttu-id="74c16-133">У объекта <a href="certificate.md"><strong>сертификата</strong></a> нет связанного закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="74c16-133">The <a href="certificate.md"><strong>Certificate</strong></a> object does not have an associated private key.</span></span><br/> <span data-ttu-id="74c16-134">Этот код ошибки возвращается при попытке подписать данные с помощью закрытого ключа подписавший, но объект <a href="certificate.md"><strong>сертификата</strong></a> , связанный с объектом- <a href="signer.md"><strong>подписавшим</strong></a> , не может использоваться для операции подписывания.</span><span class="sxs-lookup"><span data-stu-id="74c16-134">This error code is returned when an attempt is made to sign data using the signer's private key, but the <a href="certificate.md"><strong>Certificate</strong></a> object that is associated with the <a href="signer.md"><strong>Signer</strong></a> object cannot be used for the signing operation.</span></span><br/></td>
<td><span data-ttu-id="74c16-135">0x80880211</span><span class="sxs-lookup"><span data-stu-id="74c16-135">0x80880211</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-136"><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-136"><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></span></span></td>
<td><span data-ttu-id="74c16-137">Объект <a href="chain.md"><strong>цепочки</strong></a> не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="74c16-137">The <a href="chain.md"><strong>Chain</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="74c16-138">Чтобы инициализировать объект <a href="chain.md"><strong>цепочки</strong></a> , вызовите метод <a href="chain-build.md"><strong>Build</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-138">To initialize the <a href="chain.md"><strong>Chain</strong></a> object, call the <a href="chain-build.md"><strong>Build</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="74c16-139">0x80880220</span><span class="sxs-lookup"><span data-stu-id="74c16-139">0x80880220</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-140"><strong>CAPICOM_E_STORE_NOT_OPENED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-140"><strong>CAPICOM_E_STORE_NOT_OPENED</strong></span></span></td>
<td><span data-ttu-id="74c16-141">Объект <a href="store.md"><strong>Store</strong></a> не был инициализирован.</span><span class="sxs-lookup"><span data-stu-id="74c16-141">The <a href="store.md"><strong>Store</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="74c16-142">Чтобы инициализировать объект <a href="store.md"><strong>Store</strong></a> , вызовите метод <a href="store-open.md"><strong>Open</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-142">To initialize the <a href="store.md"><strong>Store</strong></a> object, call the <a href="store-open.md"><strong>Open</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="74c16-143">0x80880230</span><span class="sxs-lookup"><span data-stu-id="74c16-143">0x80880230</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-144"><strong>CAPICOM_E_STORE_EMPTY</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-144"><strong>CAPICOM_E_STORE_EMPTY</strong></span></span></td>
<td><span data-ttu-id="74c16-145">Объект <a href="store.md"><strong>хранилища</strong></a> не содержит объектов <a href="certificate.md"><strong>сертификата</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-145">The <a href="store.md"><strong>Store</strong></a> object does not contain any <a href="certificate.md"><strong>Certificate</strong></a> objects.</span></span><br/></td>
<td><span data-ttu-id="74c16-146">0x80880231</span><span class="sxs-lookup"><span data-stu-id="74c16-146">0x80880231</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-147"><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-147"><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></span></span></td>
<td><span data-ttu-id="74c16-148">Параметр <em>OpenMode</em> метода <a href="store-open.md"><strong>Store. Open</strong></a> не содержит допустимое значение CAPICOM_STORE_OPEN_MODE.</span><span class="sxs-lookup"><span data-stu-id="74c16-148">The <em>OpenMode</em> parameter of the <a href="store-open.md"><strong>Store.Open</strong></a> method does not contain a valid value of CAPICOM_STORE_OPEN_MODE.</span></span><br/> <span data-ttu-id="74c16-149">В следующем списке приведены допустимые значения CAPICOM_STORE_OPEN_MODE.</span><span class="sxs-lookup"><span data-stu-id="74c16-149">The following list shows the valid values of CAPICOM_STORE_OPEN_MODE:</span></span>
<ul>
<li><span data-ttu-id="74c16-150">CAPICOM_STORE_OPEN_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="74c16-150">CAPICOM_STORE_OPEN_READ_ONLY</span></span></li>
<li><span data-ttu-id="74c16-151">CAPICOM_STORE_OPEN_READ_WRITE</span><span class="sxs-lookup"><span data-stu-id="74c16-151">CAPICOM_STORE_OPEN_READ_WRITE</span></span></li>
<li><span data-ttu-id="74c16-152">CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="74c16-152">CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</span></span></li>
<li><span data-ttu-id="74c16-153">CAPICOM_STORE_OPEN_EXISTING_ONLY</span><span class="sxs-lookup"><span data-stu-id="74c16-153">CAPICOM_STORE_OPEN_EXISTING_ONLY</span></span></li>
<li><span data-ttu-id="74c16-154">CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</span><span class="sxs-lookup"><span data-stu-id="74c16-154">CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="74c16-155">0x80880232</span><span class="sxs-lookup"><span data-stu-id="74c16-155">0x80880232</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-156"><strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-156"><strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong></span></span></td>
<td><span data-ttu-id="74c16-157">Недопустимое значение <em>SaveAs</em> , передаваемое методу <a href="store-export.md"><strong>Export</strong></a> объекта <a href="store.md"><strong>Store</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-157">The <em>SaveAs</em> value passed to the <a href="store-export.md"><strong>Export</strong></a> method of the <a href="store.md"><strong>Store</strong></a> object was not valid.</span></span> <br/> <span data-ttu-id="74c16-158">В следующем списке приведены допустимые значения <em>SaveAs</em> :</span><span class="sxs-lookup"><span data-stu-id="74c16-158">The following list shows the valid <em>SaveAs</em> values:</span></span>
<ul>
<li><span data-ttu-id="74c16-159">CAPICOM_STORE_SAVE_AS_SERIALIZED</span><span class="sxs-lookup"><span data-stu-id="74c16-159">CAPICOM_STORE_SAVE_AS_SERIALIZED</span></span></li>
<li><span data-ttu-id="74c16-160">CAPICOM_STORE_SAVE_AS_PKCS7</span><span class="sxs-lookup"><span data-stu-id="74c16-160">CAPICOM_STORE_SAVE_AS_PKCS7</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="74c16-161">0x80880233</span><span class="sxs-lookup"><span data-stu-id="74c16-161">0x80880233</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-162"><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-162"><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="74c16-163">Свойство <a href="attribute-name.md"><strong>Name</strong></a> объекта <a href="attribute.md"><strong>Attribute</strong></a> не было инициализировано.</span><span class="sxs-lookup"><span data-stu-id="74c16-163">The <a href="attribute-name.md"><strong>Name</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="74c16-164">Задайте свойство <a href="attribute-name.md"><strong>Name</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-164">Set the <a href="attribute-name.md"><strong>Name</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="74c16-165">0x80880240</span><span class="sxs-lookup"><span data-stu-id="74c16-165">0x80880240</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-166"><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-166"><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="74c16-167">Свойство <a href="attribute-value.md"><strong>value</strong></a> объекта <a href="attribute.md"><strong>атрибута</strong></a> не было инициализировано.</span><span class="sxs-lookup"><span data-stu-id="74c16-167">The <a href="attribute-value.md"><strong>Value</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="74c16-168">Задайте свойство <a href="attribute-value.md"><strong>value</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-168">Set the <a href="attribute-value.md"><strong>Value</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="74c16-169">0x80880241</span><span class="sxs-lookup"><span data-stu-id="74c16-169">0x80880241</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-170"><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-170"><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></span></span></td>
<td><span data-ttu-id="74c16-171">Недопустимое свойство <a href="attribute-name.md"><strong>Name</strong></a> объекта <a href="attribute.md"><strong>Attribute</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-171">The <a href="attribute-name.md"><strong>Name</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="74c16-172">В следующем списке приведены допустимые имена атрибутов.</span><span class="sxs-lookup"><span data-stu-id="74c16-172">The following list shows the valid attribute names:</span></span>
<ul>
<li><span data-ttu-id="74c16-173">CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</span><span class="sxs-lookup"><span data-stu-id="74c16-173">CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</span></span></li>
<li><span data-ttu-id="74c16-174">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</span><span class="sxs-lookup"><span data-stu-id="74c16-174">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</span></span></li>
<li><span data-ttu-id="74c16-175">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="74c16-175">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="74c16-176">0x80880242</span><span class="sxs-lookup"><span data-stu-id="74c16-176">0x80880242</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-177"><strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-177"><strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong></span></span></td>
<td><span data-ttu-id="74c16-178">Свойство <a href="attribute-value.md"><strong>value</strong></a> объекта <a href="attribute.md"><strong>атрибута</strong></a> является недопустимым, так как тип данных не соответствует типу данных, указанному свойством <strong>Name</strong> .</span><span class="sxs-lookup"><span data-stu-id="74c16-178">The <a href="attribute-value.md"><strong>Value</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object is not valid because the data type does not match the data type indicated by the <strong>Name</strong> property.</span></span> <br/> <span data-ttu-id="74c16-179">Например, если свойство <a href="attribute-value.md"><strong>Name</strong></a> имеет значение CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, то тип данных должен быть <strong>Date</strong>.</span><span class="sxs-lookup"><span data-stu-id="74c16-179">For example, if the <a href="attribute-value.md"><strong>Name</strong></a> property is set to CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, the data type must be <strong>DATE</strong>.</span></span><br/></td>
<td><span data-ttu-id="74c16-180">0x80880243</span><span class="sxs-lookup"><span data-stu-id="74c16-180">0x80880243</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-181"><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-181"><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="74c16-182">Объект <a href="signer.md"><strong>подписавший</strong></a> не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="74c16-182">The <a href="signer.md"><strong>Signer</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="74c16-183">Чтобы инициализировать объект <a href="signer.md"><strong>Sign</strong></a> , задайте свойство <a href="signer-certificate.md"><strong>Certificate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-183">To initialize the <a href="signer.md"><strong>Signer</strong></a> object, set the <a href="signer-certificate.md"><strong>Certificate</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="74c16-184">0x80880250</span><span class="sxs-lookup"><span data-stu-id="74c16-184">0x80880250</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-185"><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-185"><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></span></span></td>
<td><span data-ttu-id="74c16-186">Не удается найти подписывание в объекте <a href="signeddata.md"><strong>сигнеддата</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-186">The signer cannot be found in the <a href="signeddata.md"><strong>SignedData</strong></a> object.</span></span> <br/> <span data-ttu-id="74c16-187">Как правило, это не происходит при использовании объекта <a href="signeddata.md"><strong>сигнеддата</strong></a> , созданного CAPICOM; Однако если объект <strong>сигнеддата</strong> был создан сторонним продуктом, сертификат лица может не включаться в структуру PKCS #7.</span><span class="sxs-lookup"><span data-stu-id="74c16-187">Usually, this does not happen with a <a href="signeddata.md"><strong>SignedData</strong></a> object that was created by CAPICOM; however, if the <strong>SignedData</strong> object was created by a third-party product, the signer's certificate may not be included in the PKCS #7 structure.</span></span><br/></td>
<td><span data-ttu-id="74c16-188">0x80880251</span><span class="sxs-lookup"><span data-stu-id="74c16-188">0x80880251</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-189"><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-189"><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></span></span></td>
<td><span data-ttu-id="74c16-190">Не удалось найти объект <a href="chain.md"><strong>цепочки</strong></a> в объекте- <a href="signer.md"><strong>подписавшем</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-190">A <a href="chain.md"><strong>Chain</strong></a> object cannot be found in the <a href="signer.md"><strong>Signer</strong></a> object.</span></span><br/></td>
<td><span data-ttu-id="74c16-191">0x80880252//v 2.0</span><span class="sxs-lookup"><span data-stu-id="74c16-191">0x80880252 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-192"><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-192"><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></span></span></td>
<td><span data-ttu-id="74c16-193">Предпринята попытка использовать подписывающий недопустимым образом.</span><span class="sxs-lookup"><span data-stu-id="74c16-193">An attempt is made to use the signer in a way that is not valid.</span></span><br/></td>
<td><span data-ttu-id="74c16-194">0x80880253 //v2.0</span><span class="sxs-lookup"><span data-stu-id="74c16-194">0x80880253 //v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-195"><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-195"><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="74c16-196">Объект <a href="signeddata.md"><strong>сигнеддата</strong></a> не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="74c16-196">The <a href="signeddata.md"><strong>SignedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="74c16-197">Чтобы инициализировать объект <a href="signeddata.md"><strong>сигнеддата</strong></a> , задайте свойство <a href="signeddata-content.md"><strong>Content</strong></a> или вызовите метод <a href="signeddata-verify.md"><strong>Verify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-197">To initialize the <a href="signeddata.md"><strong>SignedData</strong></a> object, set the <a href="signeddata-content.md"><strong>Content</strong></a> property or call the <a href="signeddata-verify.md"><strong>Verify</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="74c16-198">0x80880260</span><span class="sxs-lookup"><span data-stu-id="74c16-198">0x80880260</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-199"><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-199"><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="74c16-200">Объект <a href="signeddata.md"><strong>сигнеддата</strong></a> содержит недопустимый тип.</span><span class="sxs-lookup"><span data-stu-id="74c16-200">The <a href="signeddata.md"><strong>SignedData</strong></a> object contains a type that is not valid.</span></span> <br/> <span data-ttu-id="74c16-201">Как правило, это происходит при попытке проверить упакованное сообщение с помощью объекта <a href="signeddata.md"><strong>сигнеддата</strong></a> или наоборот.</span><span class="sxs-lookup"><span data-stu-id="74c16-201">Usually, this happens when an attempt is made to verify an enveloped message with a <a href="signeddata.md"><strong>SignedData</strong></a> object or vice versa.</span></span><br/></td>
<td><span data-ttu-id="74c16-202">0x80880261</span><span class="sxs-lookup"><span data-stu-id="74c16-202">0x80880261</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-203"><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-203"><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></span></span></td>
<td><span data-ttu-id="74c16-204">Объект <a href="signeddata.md"><strong>сигнеддата</strong></a> не подписан.</span><span class="sxs-lookup"><span data-stu-id="74c16-204">The <a href="signeddata.md"><strong>SignedData</strong></a> object has not been signed.</span></span> <br/> <span data-ttu-id="74c16-205">Чтобы подписать объект <a href="signeddata.md"><strong>сигнеддата</strong></a> , вызовите метод <a href="signeddata-sign.md"><strong>Sign</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-205">To sign the <a href="signeddata.md"><strong>SignedData</strong></a> object, call the <a href="signeddata-sign.md"><strong>Sign</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="74c16-206">0x80880262</span><span class="sxs-lookup"><span data-stu-id="74c16-206">0x80880262</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-207"><strong>CAPICOM_E_INVALID_ALGORITHM</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-207"><strong>CAPICOM_E_INVALID_ALGORITHM</strong></span></span></td>
<td><span data-ttu-id="74c16-208">Недопустимое значение алгоритма для свойства <a href="algorithm-name.md"><strong>Name</strong></a> объекта <a href="algorithm.md"><strong>Algorithm</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-208">The algorithm value for the <a href="algorithm-name.md"><strong>Name</strong></a> property of the <a href="algorithm.md"><strong>Algorithm</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="74c16-209">В следующем списке показаны допустимые значения алгоритма для свойства <a href="algorithm-name.md"><strong>Name</strong></a> :</span><span class="sxs-lookup"><span data-stu-id="74c16-209">The following list shows the valid algorithm values for the <a href="algorithm-name.md"><strong>Name</strong></a> property:</span></span>
<ul>
<li><span data-ttu-id="74c16-210">CAPICOM_ENCRYPTION_ALGORITHM_RC2</span><span class="sxs-lookup"><span data-stu-id="74c16-210">CAPICOM_ENCRYPTION_ALGORITHM_RC2</span></span></li>
<li><span data-ttu-id="74c16-211">CAPICOM_ENCRYPTION_ALGORITHM_RC4</span><span class="sxs-lookup"><span data-stu-id="74c16-211">CAPICOM_ENCRYPTION_ALGORITHM_RC4</span></span></li>
<li><span data-ttu-id="74c16-212">CAPICOM_ENCRYPTION_ALGORITHM_DES</span><span class="sxs-lookup"><span data-stu-id="74c16-212">CAPICOM_ENCRYPTION_ALGORITHM_DES</span></span></li>
<li><span data-ttu-id="74c16-213">CAPICOM_ENCRYPTION_ALGORITHM_3DES</span><span class="sxs-lookup"><span data-stu-id="74c16-213">CAPICOM_ENCRYPTION_ALGORITHM_3DES</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="74c16-214">0x80880270</span><span class="sxs-lookup"><span data-stu-id="74c16-214">0x80880270</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-215"><strong>CAPICOM_E_INVALID_KEY_LENGTH</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-215"><strong>CAPICOM_E_INVALID_KEY_LENGTH</strong></span></span></td>
<td><span data-ttu-id="74c16-216">Недопустимое значение длины ключа для свойства <a href="algorithm-keylength.md"><strong>keylength</strong></a> объекта <a href="algorithm.md"><strong>Algorithm</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-216">The key length value for the <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> property of the <a href="algorithm.md"><strong>Algorithm</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="74c16-217">В следующем списке приведены допустимые значения длины ключа для свойства <a href="algorithm-keylength.md"><strong>keylength</strong></a> :</span><span class="sxs-lookup"><span data-stu-id="74c16-217">The following list shows the valid key length values for the <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> property:</span></span>
<ul>
<li><span data-ttu-id="74c16-218">CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</span><span class="sxs-lookup"><span data-stu-id="74c16-218">CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</span></span></li>
<li><span data-ttu-id="74c16-219">CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</span><span class="sxs-lookup"><span data-stu-id="74c16-219">CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</span></span></li>
<li><span data-ttu-id="74c16-220">CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</span><span class="sxs-lookup"><span data-stu-id="74c16-220">CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</span></span></li>
<li><span data-ttu-id="74c16-221">CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</span><span class="sxs-lookup"><span data-stu-id="74c16-221">CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="74c16-222">0x80880271</span><span class="sxs-lookup"><span data-stu-id="74c16-222">0x80880271</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-223"><strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-223"><strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="74c16-224">Объект <a href="envelopeddata.md"><strong>енвелопеддата</strong></a> не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="74c16-224">The <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="74c16-225">Чтобы инициализировать объект <a href="envelopeddata.md"><strong>енвелопеддата</strong></a> , необходимо либо задать свойство <a href="envelopeddata-content.md"><strong>Content</strong></a> , либо вызвать метод <a href="envelopeddata-decrypt.md"><strong>дешифровки</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-225">To initialize the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object, either set the <a href="envelopeddata-content.md"><strong>Content</strong></a> property or call the <a href="envelopeddata-decrypt.md"><strong>Decrypt</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="74c16-226">0x80880280</span><span class="sxs-lookup"><span data-stu-id="74c16-226">0x80880280</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-227"><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-227"><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="74c16-228">Объект <a href="envelopeddata.md"><strong>енвелопеддата</strong></a> содержит недопустимый тип.</span><span class="sxs-lookup"><span data-stu-id="74c16-228">The <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object contains a type that is not valid.</span></span> <br/> <span data-ttu-id="74c16-229">Обычно это происходит при попытке проверить подписанное сообщение с помощью объекта <a href="envelopeddata.md"><strong>енвелопеддата</strong></a> или наоборот.</span><span class="sxs-lookup"><span data-stu-id="74c16-229">Usually, this happens when an attempt is made to verify a signed message with an <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object or vice versa.</span></span><br/></td>
<td><span data-ttu-id="74c16-230">0x80880281</span><span class="sxs-lookup"><span data-stu-id="74c16-230">0x80880281</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-231"><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-231"><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></span></span></td>
<td><span data-ttu-id="74c16-232">При вызове метода <a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a> объекта <strong>Енвелопеддата</strong> в объекте <a href="envelopeddata.md"><strong>енвелопеддата</strong></a> не указан получатель.</span><span class="sxs-lookup"><span data-stu-id="74c16-232">There is no recipient specified in the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object when the <a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a> method of an <strong>EnvelopedData</strong> object is called.</span></span> <br/> <span data-ttu-id="74c16-233">Чтобы добавить получателя, вызовите метод <a href="recipients-add.md"><strong>Recipients. Add</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-233">To add a recipient, call the <a href="recipients-add.md"><strong>Recipients.Add</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="74c16-234">0x80880282</span><span class="sxs-lookup"><span data-stu-id="74c16-234">0x80880282</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-235"><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-235"><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></span></span></td>
<td><span data-ttu-id="74c16-236">Не удается найти получателя в объекте <a href="envelopeddata.md"><strong>енвелопеддата</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-236">The recipient cannot be found in the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object.</span></span> <br/> <span data-ttu-id="74c16-237">Как правило, это не происходит с объектом <a href="envelopeddata.md"><strong>енвелопеддата</strong></a> , созданным CAPICOM; Однако если объект <strong>енвелопеддата</strong> был создан сторонним продуктом, сертификат получателя может не включаться в структуру PKCS #7.</span><span class="sxs-lookup"><span data-stu-id="74c16-237">Usually, this does not happen with an <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object that was created by CAPICOM; however, if the <strong>EnvelopedData</strong> object was created by a third-party product, the recipient's certificate may not be included in the PKCS #7 structure.</span></span><br/></td>
<td><span data-ttu-id="74c16-238">0x80880283</span><span class="sxs-lookup"><span data-stu-id="74c16-238">0x80880283</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-239"><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-239"><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="74c16-240">Объект <a href="encrypteddata.md"><strong>EncryptedData</strong></a> не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="74c16-240">The <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="74c16-241">Чтобы инициализировать объект <a href="encrypteddata.md"><strong>EncryptedData</strong></a> , необходимо либо задать свойство <a href="encrypteddata-content.md"><strong>Content</strong></a> , либо вызвать метод <a href="encrypteddata-decrypt.md"><strong>дешифровки</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-241">To initialize the <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object, either set the <a href="encrypteddata-content.md"><strong>Content</strong></a> property or call the <a href="encrypteddata-decrypt.md"><strong>Decrypt</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="74c16-242">0x80880290</span><span class="sxs-lookup"><span data-stu-id="74c16-242">0x80880290</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-243"><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-243"><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="74c16-244">Объект <a href="encrypteddata.md"><strong>EncryptedData</strong></a> имеет недопустимый тип.</span><span class="sxs-lookup"><span data-stu-id="74c16-244">The <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object is not a valid type.</span></span> <br/> <span data-ttu-id="74c16-245">Обычно это означает, что данные повреждены.</span><span class="sxs-lookup"><span data-stu-id="74c16-245">Usually, this means the data is corrupted.</span></span><br/></td>
<td><span data-ttu-id="74c16-246">0x80880291</span><span class="sxs-lookup"><span data-stu-id="74c16-246">0x80880291</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-247"><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-247"><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></span></span></td>
<td><span data-ttu-id="74c16-248">Секрет объекта <a href="encrypteddata.md"><strong>EncryptedData</strong></a> не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="74c16-248">The secret of an <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="74c16-249">Чтобы инициализировать секрет объекта <a href="encrypteddata.md"><strong>EncryptedData</strong></a> , вызовите метод <a href="encrypteddata-setsecret.md"><strong>сетсекрет</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-249">To initialize the secret of an <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object, call the <a href="encrypteddata-setsecret.md"><strong>SetSecret</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="74c16-250">0x80880292</span><span class="sxs-lookup"><span data-stu-id="74c16-250">0x80880292</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-251"><strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-251"><strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="74c16-252">Объект <a href="privatekey.md"><strong>PrivateKey</strong></a> не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="74c16-252">The <a href="privatekey.md"><strong>PrivateKey</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="74c16-253">0x80880300//v 2.0</span><span class="sxs-lookup"><span data-stu-id="74c16-253">0x80880300 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-254"><strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-254"><strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong></span></span></td>
<td><span data-ttu-id="74c16-255">Не удается экспортировать объект <a href="privatekey.md"><strong>PrivateKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-255">The <a href="privatekey.md"><strong>PrivateKey</strong></a> object cannot be exported.</span></span><br/></td>
<td><span data-ttu-id="74c16-256">0x80880301//v 2.0</span><span class="sxs-lookup"><span data-stu-id="74c16-256">0x80880301 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-257"><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-257"><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="74c16-258">Объект <a href="encodeddata.md"><strong>енкодеддата</strong></a> не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="74c16-258">The <a href="encodeddata.md"><strong>EncodedData</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="74c16-259">0x80880320//v 2.0</span><span class="sxs-lookup"><span data-stu-id="74c16-259">0x80880320 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-260"><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-260"><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="74c16-261">Объект <a href="extension.md"><strong>расширения</strong></a> не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="74c16-261">The <a href="extension.md"><strong>Extension</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="74c16-262">0x80880330//v 2.0</span><span class="sxs-lookup"><span data-stu-id="74c16-262">0x80880330 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-263"><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-263"><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="74c16-264">Свойство <a href="extendedproperty-propid.md"><strong>PropID</strong></a> объекта <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> не инициализировано.</span><span class="sxs-lookup"><span data-stu-id="74c16-264">The <a href="extendedproperty-propid.md"><strong>PropID</strong></a> property of the <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="74c16-265">0x80880340//v 2.0</span><span class="sxs-lookup"><span data-stu-id="74c16-265">0x80880340 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-266"><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-266"><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="74c16-267">Параметр <em>FindType</em> метода <a href="certificates-find.md"><strong>Certificates. Find</strong></a> не является значением перечисления <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-267">The <em>FindType</em> parameter of the <a href="certificates-find.md"><strong>Certificates.Find</strong></a> method is not a value of the <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> enumeration.</span></span><br/></td>
<td><span data-ttu-id="74c16-268">0x80880350//v 2.0</span><span class="sxs-lookup"><span data-stu-id="74c16-268">0x80880350 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-269"><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-269"><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></span></span></td>
<td><span data-ttu-id="74c16-270">Указана недопустимая Предопределенная политика для операции поиска.</span><span class="sxs-lookup"><span data-stu-id="74c16-270">The specified predefined policy for the find operation is not valid.</span></span><br/></td>
<td><span data-ttu-id="74c16-271">0x80880351//v 2.0</span><span class="sxs-lookup"><span data-stu-id="74c16-271">0x80880351 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-272"><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-272"><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="74c16-273">Объект <a href="signedcode.md"><strong>сигнедкоде</strong></a> не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="74c16-273">The <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="74c16-274">0x80880360//v 2.0</span><span class="sxs-lookup"><span data-stu-id="74c16-274">0x80880360 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-275"><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-275"><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></span></span></td>
<td><span data-ttu-id="74c16-276">Объект <a href="signedcode.md"><strong>сигнедкоде</strong></a> не подписан.</span><span class="sxs-lookup"><span data-stu-id="74c16-276">The <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been signed.</span></span><br/> <span data-ttu-id="74c16-277">Чтобы подписать объект <a href="signedcode.md"><strong>сигнедкоде</strong></a> , вызовите метод <a href="signedcode-sign.md"><strong>Sign</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-277">To sign the <a href="signedcode.md"><strong>SignedCode</strong></a> object, call the <a href="signedcode-sign.md"><strong>Sign</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="74c16-278">0x80880361//v 2.0</span><span class="sxs-lookup"><span data-stu-id="74c16-278">0x80880361 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-279"><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-279"><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="74c16-280">Свойство <a href="signedcode-description.md"><strong>Description</strong></a> объекта <a href="signedcode.md"><strong>сигнедкоде</strong></a> не инициализировано.</span><span class="sxs-lookup"><span data-stu-id="74c16-280">The <a href="signedcode-description.md"><strong>Description</strong></a> property of the <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="74c16-281">0x80880362//v 2.0</span><span class="sxs-lookup"><span data-stu-id="74c16-281">0x80880362 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-282"><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-282"><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="74c16-283">Свойство <a href="signedcode-descriptionurl.md"><strong>дескриптионурл</strong></a> объекта <a href="signedcode.md"><strong>сигнедкоде</strong></a> не инициализировано.</span><span class="sxs-lookup"><span data-stu-id="74c16-283">The <a href="signedcode-descriptionurl.md"><strong>DescriptionURL</strong></a> property of the <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="74c16-284">0x80880363//v 2.0</span><span class="sxs-lookup"><span data-stu-id="74c16-284">0x80880363 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-285"><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-285"><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></span></span></td>
<td><span data-ttu-id="74c16-286">Недопустимый параметр <em>URL-адреса</em> метода <a href="signedcode-timestamp.md"><strong>сигнедкоде. timestamp</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-286">The <em>URL</em> parameter of the <a href="signedcode-timestamp.md"><strong>SignedCode.Timestamp</strong></a> method is not valid.</span></span><br/></td>
<td><span data-ttu-id="74c16-287">0x80880364//v 2.0</span><span class="sxs-lookup"><span data-stu-id="74c16-287">0x80880364 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-288"><strong>CAPICOM_E_HASH_NO_DATA</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-288"><strong>CAPICOM_E_HASH_NO_DATA</strong></span></span></td>
<td><span data-ttu-id="74c16-289">Объект <a href="hasheddata.md"><strong>хашеддата</strong></a> не содержит данных.</span><span class="sxs-lookup"><span data-stu-id="74c16-289">The <a href="hasheddata.md"><strong>HashedData</strong></a> object does not contain any data.</span></span><br/></td>
<td><span data-ttu-id="74c16-290">0x80880370//v 2.0</span><span class="sxs-lookup"><span data-stu-id="74c16-290">0x80880370 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-291"><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-291"><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></span></span></td>
<td><span data-ttu-id="74c16-292">Недопустимый тип преобразования.</span><span class="sxs-lookup"><span data-stu-id="74c16-292">The convert type is not valid.</span></span><br/></td>
<td><span data-ttu-id="74c16-293">0x80880380//v 2.0</span><span class="sxs-lookup"><span data-stu-id="74c16-293">0x80880380 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-294"><strong>CAPICOM_E_NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-294"><strong>CAPICOM_E_NOT_SUPPORTED</strong></span></span></td>
<td><span data-ttu-id="74c16-295">Запрошенная операция не поддерживается на текущей платформе.</span><span class="sxs-lookup"><span data-stu-id="74c16-295">The requested operation is not supported in the current platform.</span></span> <br/></td>
<td><span data-ttu-id="74c16-296">0x80880900</span><span class="sxs-lookup"><span data-stu-id="74c16-296">0x80880900</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-297"><strong>CAPICOM_E_UI_DISABLED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-297"><strong>CAPICOM_E_UI_DISABLED</strong></span></span></td>
<td><span data-ttu-id="74c16-298">При подписывании свойство <a href="signer-certificate.md"><strong>сертификата</strong></a> объекта <a href="signer.md"><strong>подписавши</strong></a> не было задано, но запрос сертификата пользователя был отключен.</span><span class="sxs-lookup"><span data-stu-id="74c16-298">When signing, the <a href="signer-certificate.md"><strong>Certificate</strong></a> property of the <a href="signer.md"><strong>Signer</strong></a> object has not been set, but the prompt for the user certificate has been disabled.</span></span> <br/> <span data-ttu-id="74c16-299">Либо включите запрос, задавая свойство <a href="settings-enablepromptforcertificateui.md"><strong>енаблепромптфорцертификатеуи</strong></a> объекта <a href="settings.md"><strong>Settings</strong></a> , либо задайте свойство <a href="signer-certificate.md"><strong>Certificate</strong></a> объекта <a href="signer.md"><strong>Sign</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="74c16-299">Either enable the prompt by setting the <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> property of the <a href="settings.md"><strong>Settings</strong></a> object, or set the <a href="signer-certificate.md"><strong>Certificate</strong></a> property of the <a href="signer.md"><strong>Signer</strong></a> object.</span></span><br/></td>
<td><span data-ttu-id="74c16-300">0x80880901</span><span class="sxs-lookup"><span data-stu-id="74c16-300">0x80880901</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-301"><strong>CAPICOM_E_CANCELLED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-301"><strong>CAPICOM_E_CANCELLED</strong></span></span></td>
<td><span data-ttu-id="74c16-302">Операция отменена пользователем.</span><span class="sxs-lookup"><span data-stu-id="74c16-302">The operation has been canceled by the user.</span></span> <br/> <span data-ttu-id="74c16-303">Это происходит, когда пользователю предлагается разрешение на выполнение определенной операции, например доступ к закрытому ключу, и пользователь отменяет операцию.</span><span class="sxs-lookup"><span data-stu-id="74c16-303">This happens when the user is prompted for permission to carry out a certain operation, such as accessing the private key, and the user cancels the operation.</span></span><br/></td>
<td><span data-ttu-id="74c16-304">0x80880902</span><span class="sxs-lookup"><span data-stu-id="74c16-304">0x80880902</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-305"><strong>CAPICOM_E_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-305"><strong>CAPICOM_E_NOT_ALLOWED</strong></span></span></td>
<td><span data-ttu-id="74c16-306">Предпринятая операция не разрешена.</span><span class="sxs-lookup"><span data-stu-id="74c16-306">The attempted operation is not allowed.</span></span><br/> <span data-ttu-id="74c16-307">Например, изменение свойства <a href="extendedproperty-propid.md"><strong>PropID</strong></a> объекта <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> не допускается, если объект присоединен к сертификату.</span><span class="sxs-lookup"><span data-stu-id="74c16-307">For example, changing the <a href="extendedproperty-propid.md"><strong>PropID</strong></a> property of an <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> object is not allowed if the object is attached to a certificate.</span></span><br/></td>
<td><span data-ttu-id="74c16-308">0x80880903//v 2.0</span><span class="sxs-lookup"><span data-stu-id="74c16-308">0x80880903 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-309"><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-309"><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></span></span></td>
<td><span data-ttu-id="74c16-310">Элемент CAPICOM запустил ресурс.</span><span class="sxs-lookup"><span data-stu-id="74c16-310">CAPICOM has run out of a resource.</span></span><br/></td>
<td><span data-ttu-id="74c16-311">0x80880904//v 2.0</span><span class="sxs-lookup"><span data-stu-id="74c16-311">0x80880904 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c16-312"><strong>CAPICOM_E_INTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-312"><strong>CAPICOM_E_INTERNAL</strong></span></span></td>
<td><span data-ttu-id="74c16-313">Произошла внутренняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="74c16-313">An internal error has occurred.</span></span> <br/> <span data-ttu-id="74c16-314">Обратитесь за помощью в службу технической поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="74c16-314">Contact Microsoft Technical Support for assistance.</span></span><br/></td>
<td><span data-ttu-id="74c16-315">0x80880911</span><span class="sxs-lookup"><span data-stu-id="74c16-315">0x80880911</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c16-316"><strong>CAPICOM_E_UNKNOWN</strong></span><span class="sxs-lookup"><span data-stu-id="74c16-316"><strong>CAPICOM_E_UNKNOWN</strong></span></span></td>
<td><span data-ttu-id="74c16-317">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="74c16-317">An unknown error has occurred.</span></span> <br/> <span data-ttu-id="74c16-318">Собирайте как можно больше информации и обратитесь к поставщику.</span><span class="sxs-lookup"><span data-stu-id="74c16-318">Collect as much information as possible, and contact your vendor.</span></span><br/></td>
<td><span data-ttu-id="74c16-319">0x80880999</span><span class="sxs-lookup"><span data-stu-id="74c16-319">0x80880999</span></span></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="74c16-320">Требования</span><span class="sxs-lookup"><span data-stu-id="74c16-320">Requirements</span></span>



| <span data-ttu-id="74c16-321">Требование</span><span class="sxs-lookup"><span data-stu-id="74c16-321">Requirement</span></span> | <span data-ttu-id="74c16-322">Значение</span><span class="sxs-lookup"><span data-stu-id="74c16-322">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="74c16-323">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="74c16-323">Redistributable</span></span><br/> | <span data-ttu-id="74c16-324">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="74c16-324">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="74c16-325">Header</span><span class="sxs-lookup"><span data-stu-id="74c16-325">Header</span></span><br/>          | <dl> <span data-ttu-id="74c16-326"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="74c16-326"><dt>Capicom.h</dt></span></span> </dl> |



 

 




