---
description: Библиотека CertEnroll.dll реализует пять интерфейсов, которые можно использовать для создания запроса сертификата и управления им.
ms.assetid: f4630095-6ba2-46f7-8825-e7a5b1cb185a
title: Функции запроса сертификата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04191f49949f662a9b9d780726f7ac7a40b370ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080357"
---
# <a name="certificate-request-functions"></a><span data-ttu-id="fa567-103">Функции запроса сертификата</span><span class="sxs-lookup"><span data-stu-id="fa567-103">Certificate Request Functions</span></span>

<span data-ttu-id="fa567-104">Библиотека CertEnroll.dll реализует пять интерфейсов, которые можно использовать для создания запроса сертификата и управления им.</span><span class="sxs-lookup"><span data-stu-id="fa567-104">The CertEnroll.dll library implements five interfaces that can be used to create and manage a certificate request.</span></span> <span data-ttu-id="fa567-105">Из них интерфейс [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) представляет абстрактный базовый объект, определяющий сигнатуры методов, наследуемые следующими четырьмя интерфейсами.</span><span class="sxs-lookup"><span data-stu-id="fa567-105">Of these, the [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) interface represents an abstract base object that defines method signatures inherited by the following four interfaces.</span></span>

| <span data-ttu-id="fa567-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="fa567-106">Interface</span></span>                                                                        | <span data-ttu-id="fa567-107">Описание</span><span class="sxs-lookup"><span data-stu-id="fa567-107">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa567-108">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="fa567-108">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | <span data-ttu-id="fa567-109">Позволяет создавать сертификаты напрямую без применения к [*центру сертификации*](/windows/desktop/SecGloss/c-gly) (ЦС).</span><span class="sxs-lookup"><span data-stu-id="fa567-109">Enables you to create a certificate directly without applying to a [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA).</span></span><br/>                                                                                                            |
| [<span data-ttu-id="fa567-110">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="fa567-110">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | <span data-ttu-id="fa567-111">Представляет [*Управление сертификатами через CMS*](/windows/desktop/SecGloss/c-gly) (CMC) (сообщение управления сертификатами через CMS), которое может содержать вложенный \# запрос PKCS 10 или другой объект запроса CMC.</span><span class="sxs-lookup"><span data-stu-id="fa567-111">Represents a [*Certificate Management over CMS*](/windows/desktop/SecGloss/c-gly) (CMC) (Certificate Management Message over CMS) certificate request that can contain a nested PKCS \#10 request or another CMC request object.</span></span><br/> |
| [<span data-ttu-id="fa567-112">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="fa567-112">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | <span data-ttu-id="fa567-113">Представляет объект запроса синтаксиса сообщения [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) (CMS), который должен содержать вложенный \# запрос PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="fa567-113">Represents a [*PKCS \#7*](/windows/desktop/SecGloss/p-gly) certificate message syntax (CMS) request object that must contain a nested PKCS \#10 request.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="fa567-114">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="fa567-114">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | <span data-ttu-id="fa567-115">Представляет \# запрос сертификата PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="fa567-115">Represents a PKCS \#10 certificate request.</span></span> <span data-ttu-id="fa567-116">Запрос PKCS \# 10 может быть отправлен непосредственно в центр сертификации или может быть заключен в \# запрос PKCS 7 или CMC.</span><span class="sxs-lookup"><span data-stu-id="fa567-116">A PKCS \#10 request can be sent directly to a CA, or it can be wrapped by a PKCS \#7 or CMC request.</span></span><br/>                                                                                                                                                            |



 

<span data-ttu-id="fa567-117">Объект запроса сертификата можно использовать для инициализации объекта [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) для регистрации клиента в иерархии сертификатов и установки ответа сертификата, возвращенного ЦС.</span><span class="sxs-lookup"><span data-stu-id="fa567-117">You can use a certificate request object to initialize an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object to enroll a client in a certificate hierarchy and install the certificate response returned by the CA.</span></span>

<span data-ttu-id="fa567-118">В каждом из следующих разделов указывается функция, экспортируемая с помощью Xenroll.dll для создания, перечисления или удаления запросов сертификатов.</span><span class="sxs-lookup"><span data-stu-id="fa567-118">Each of the following sections identifies a function exported by Xenroll.dll to create, enumerate, or delete certificate requests.</span></span> <span data-ttu-id="fa567-119">В каждом разделе также обсуждается использование CertEnroll.dll для замены функции или указывает, что сопоставление между двумя библиотеками не существует:</span><span class="sxs-lookup"><span data-stu-id="fa567-119">Each section also discusses how to use CertEnroll.dll to replace the function or indicates that no mapping between the two libraries exists:</span></span>

-   [<span data-ttu-id="fa567-120">createFilePKCS10WStr</span><span class="sxs-lookup"><span data-stu-id="fa567-120">createFilePKCS10WStr</span></span>](#createfilepkcs10wstr)
-   [<span data-ttu-id="fa567-121">креатефилерекуествстр</span><span class="sxs-lookup"><span data-stu-id="fa567-121">createFileRequestWStr</span></span>](#createfilerequestwstr)
-   [<span data-ttu-id="fa567-122">createPKCS10WStr</span><span class="sxs-lookup"><span data-stu-id="fa567-122">createPKCS10WStr</span></span>](#createpkcs10wstr)
-   [<span data-ttu-id="fa567-123">CreatePKCS7RequestFromRequest</span><span class="sxs-lookup"><span data-stu-id="fa567-123">CreatePKCS7RequestFromRequest</span></span>](#createpkcs7requestfromrequest)
-   [<span data-ttu-id="fa567-124">креатерекуествстр</span><span class="sxs-lookup"><span data-stu-id="fa567-124">createRequestWStr</span></span>](#createrequestwstr)
-   [<span data-ttu-id="fa567-125">делетерекуестцерт</span><span class="sxs-lookup"><span data-stu-id="fa567-125">DeleteRequestCert</span></span>](#deleterequestcert)
-   [<span data-ttu-id="fa567-126">енумпендингрекуествстр</span><span class="sxs-lookup"><span data-stu-id="fa567-126">enumPendingRequestWStr</span></span>](#enumpendingrequestwstr)
-   [<span data-ttu-id="fa567-127">ремовепендингрекуествстр</span><span class="sxs-lookup"><span data-stu-id="fa567-127">removePendingRequestWStr</span></span>](#removependingrequestwstr)
-   [<span data-ttu-id="fa567-128">Сброс</span><span class="sxs-lookup"><span data-stu-id="fa567-128">Reset</span></span>](#reset)
-   [<span data-ttu-id="fa567-129">сетпендингрекуестинфовстр</span><span class="sxs-lookup"><span data-stu-id="fa567-129">setPendingRequestInfoWStr</span></span>](#setpendingrequestinfowstr)
-   [<span data-ttu-id="fa567-130">См. также</span><span class="sxs-lookup"><span data-stu-id="fa567-130">Related topics</span></span>](#related-topics)

## <a name="createfilepkcs10wstr"></a><span data-ttu-id="fa567-131">createFilePKCS10WStr</span><span class="sxs-lookup"><span data-stu-id="fa567-131">createFilePKCS10WStr</span></span>

<span data-ttu-id="fa567-132">Функция [**createFilePKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr) в Xenroll.dll создает запрос сертификата PKCS 10 в кодировке Base64 \# и сохраняет его в файле.</span><span class="sxs-lookup"><span data-stu-id="fa567-132">The [**createFilePKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr) function in Xenroll.dll creates a base64-encoded PKCS \#10 certificate request and saves it in a file.</span></span>

<span data-ttu-id="fa567-133">Библиотека CertEnroll.dll не реализует напрямую функции для записи запроса в файл.</span><span class="sxs-lookup"><span data-stu-id="fa567-133">The CertEnroll.dll library does not directly implement functionality to write a request to a file.</span></span> <span data-ttu-id="fa567-134">Однако можно получить запрос на сертификат, вызвав свойство [**rawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) объекта [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) и создав пользовательскую функцию для копирования значения в файл.</span><span class="sxs-lookup"><span data-stu-id="fa567-134">You can, however, retrieve a certificate request by calling the [**RawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) property on the [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) object and creating a custom function to copy the value to a file.</span></span>

## <a name="createfilerequestwstr"></a><span data-ttu-id="fa567-135">креатефилерекуествстр</span><span class="sxs-lookup"><span data-stu-id="fa567-135">createFileRequestWStr</span></span>

<span data-ttu-id="fa567-136">Функция [**креатефилерекуествстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilerequestwstr) в Xenroll.dll создает \# запрос сертификата PKCS 7, PKCS \# 10 или CMC и сохраняет его в файле.</span><span class="sxs-lookup"><span data-stu-id="fa567-136">The [**createFileRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilerequestwstr) function in Xenroll.dll creates a PKCS \#7, PKCS \#10, or CMC certificate request and saves it in a file.</span></span>

<span data-ttu-id="fa567-137">Библиотека CertEnroll.dll не реализует напрямую функции для записи запроса в файл.</span><span class="sxs-lookup"><span data-stu-id="fa567-137">The CertEnroll.dll library does not directly implement functionality to write a request to a file.</span></span> <span data-ttu-id="fa567-138">Однако можно получить запрос на сертификат, вызвав свойство [**rawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) объекта [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) и создав пользовательскую функцию для копирования значения в файл.</span><span class="sxs-lookup"><span data-stu-id="fa567-138">You can, however, retrieve a certificate request by calling the [**RawData**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_rawdata) property on the [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) object and creating a custom function to copy the value to a file.</span></span>

## <a name="createpkcs10wstr"></a><span data-ttu-id="fa567-139">createPKCS10WStr</span><span class="sxs-lookup"><span data-stu-id="fa567-139">createPKCS10WStr</span></span>

<span data-ttu-id="fa567-140">Функция [**createPKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr) в Xenroll.dll создает \# запрос сертификата PKCS 10 и копирует его в массив байтов.</span><span class="sxs-lookup"><span data-stu-id="fa567-140">The [**createPKCS10WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr) function in Xenroll.dll creates a PKCS \#10 certificate request and copies it to a byte array.</span></span>

<span data-ttu-id="fa567-141">Вы можете использовать объект [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) для инициализации \# запроса PKCS 10 из существующего запроса, существующего сертификата, [*закрытого ключа*](/windows/desktop/SecGloss/p-gly), [*открытого ключа*](/windows/desktop/SecGloss/p-gly)или шаблона.</span><span class="sxs-lookup"><span data-stu-id="fa567-141">You can use an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object to initialize a PKCS \#10 request from an existing request, an existing certificate, a [*private key*](/windows/desktop/SecGloss/p-gly), a [*public key*](/windows/desktop/SecGloss/p-gly), or a template.</span></span>

## <a name="createpkcs7requestfromrequest"></a><span data-ttu-id="fa567-142">CreatePKCS7RequestFromRequest</span><span class="sxs-lookup"><span data-stu-id="fa567-142">CreatePKCS7RequestFromRequest</span></span>

<span data-ttu-id="fa567-143">Функция [**CreatePKCS7RequestFromRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs7requestfromrequest) в Xenroll.dll создает \# запрос сертификата PKCS 7 и копирует его в массив байтов.</span><span class="sxs-lookup"><span data-stu-id="fa567-143">The [**CreatePKCS7RequestFromRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs7requestfromrequest) function in Xenroll.dll creates a PKCS \#7 certificate request and copies it to a byte array.</span></span>

<span data-ttu-id="fa567-144">Вы можете использовать объект [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) для инициализации \# запроса PKCS 7 из существующего запроса, существующего сертификата, объекта внутреннего запроса или шаблона.</span><span class="sxs-lookup"><span data-stu-id="fa567-144">You can use an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object to initialize a PKCS \#7 request from an existing request, an existing certificate, an inner request object, or a template.</span></span>

## <a name="createrequestwstr"></a><span data-ttu-id="fa567-145">креатерекуествстр</span><span class="sxs-lookup"><span data-stu-id="fa567-145">createRequestWStr</span></span>

<span data-ttu-id="fa567-146">Функция [**креатерекуествстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createrequestwstr) в Xenroll.dll создает \# запрос сертификата PKCS 7, PKCS \# 10 или CMC и копирует его в массив байтов.</span><span class="sxs-lookup"><span data-stu-id="fa567-146">The [**createRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createrequestwstr) function in Xenroll.dll creates a PKCS \#7, PKCS \#10, or CMC certificate request and copies it to a byte array.</span></span>

<span data-ttu-id="fa567-147">Чтобы использовать библиотеку CertEnroll.dll для создания запросов PKCS \# 7, PKCS \# 10 или CMC, можно создать и инициализировать экземпляры объектов [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7), [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)или [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="fa567-147">To use the CertEnroll.dll library to create PKCS \#7, PKCS \#10, or CMC requests, you can create and initialize instances of the [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7), [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10), or [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) objects.</span></span>

## <a name="deleterequestcert"></a><span data-ttu-id="fa567-148">делетерекуестцерт</span><span class="sxs-lookup"><span data-stu-id="fa567-148">DeleteRequestCert</span></span>

<span data-ttu-id="fa567-149">Функция [**делетерекуестцерт**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_deleterequestcert) в Xenroll.dll указывает или получает логическое значение, указывающее, удаляется ли фиктивный сертификат после установки ответа на сертификат.</span><span class="sxs-lookup"><span data-stu-id="fa567-149">The [**DeleteRequestCert**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_deleterequestcert) function in Xenroll.dll specifies or retrieves a Boolean value that indicates whether a dummy certificate is removed after a certificate response has been installed.</span></span>

<span data-ttu-id="fa567-150">Объект [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) в CertEnroll.dll автоматически создает фиктивные сертификаты в хранилище запросов для временного сохранения различных свойств сертификата, которые инициализируются во время процесса регистрации.</span><span class="sxs-lookup"><span data-stu-id="fa567-150">The [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object in CertEnroll.dll automatically creates dummy certificates in the request store to temporarily save various certificate properties that are initialized during the enrollment process.</span></span> <span data-ttu-id="fa567-151">После выдачи сертификата центром сертификации свойства копируются в новый сертификат и удаляется фиктивный сертификат.</span><span class="sxs-lookup"><span data-stu-id="fa567-151">After a certificate is issued by a CA, the properties are copied to the new certificate and the dummy certificate is deleted.</span></span> <span data-ttu-id="fa567-152">Библиотека CertEnroll.dll не позволяет принудительно оставаться фиктивным сертификатом после установки ответа на сертификат.</span><span class="sxs-lookup"><span data-stu-id="fa567-152">The CertEnroll.dll library does not allow you to force a dummy certificate to remain after the certificate response has been installed.</span></span>

## <a name="enumpendingrequestwstr"></a><span data-ttu-id="fa567-153">енумпендингрекуествстр</span><span class="sxs-lookup"><span data-stu-id="fa567-153">enumPendingRequestWStr</span></span>

<span data-ttu-id="fa567-154">Функция [**енумпендингрекуествстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-enumpendingrequestwstr) в Xenroll.dll извлекает указанное значение свойства для ожидающего запроса.</span><span class="sxs-lookup"><span data-stu-id="fa567-154">The [**enumPendingRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-enumpendingrequestwstr) function in Xenroll.dll retrieves a specified property value for a pending request.</span></span>

<span data-ttu-id="fa567-155">Библиотека CertEnroll.dll напрямую не реализует функции для удаления ожидающего запроса на сертификат.</span><span class="sxs-lookup"><span data-stu-id="fa567-155">The CertEnroll.dll library does not directly implement functionality to remove a pending certificate request.</span></span>

## <a name="removependingrequestwstr"></a><span data-ttu-id="fa567-156">ремовепендингрекуествстр</span><span class="sxs-lookup"><span data-stu-id="fa567-156">removePendingRequestWStr</span></span>

<span data-ttu-id="fa567-157">Функция [**ремовепендингрекуествстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-removependingrequestwstr) в Xenroll.dll Удаляет ожидающий запрос из хранилища запросов.</span><span class="sxs-lookup"><span data-stu-id="fa567-157">The [**removePendingRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-removependingrequestwstr) function in Xenroll.dll removes a pending request from the request store.</span></span>

<span data-ttu-id="fa567-158">Библиотека CertEnroll.dll напрямую не реализует функции для удаления ожидающего запроса на сертификат.</span><span class="sxs-lookup"><span data-stu-id="fa567-158">The CertEnroll.dll library does not directly implement functionality to remove a pending certificate request.</span></span>

## <a name="reset"></a><span data-ttu-id="fa567-159">Reset</span><span class="sxs-lookup"><span data-stu-id="fa567-159">Reset</span></span>

<span data-ttu-id="fa567-160">Функция [**Reset**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-reset) в Xenroll.dll возвращает управление регистрацией сертификата в исходное состояние.</span><span class="sxs-lookup"><span data-stu-id="fa567-160">The [**Reset**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-reset) function in Xenroll.dll returns the Certificate Enrollment Control to an initial state.</span></span>

<span data-ttu-id="fa567-161">Тот же результат можно получить с помощью Certenroll.dll, чтобы создать новый объект запроса для требуемого типа.</span><span class="sxs-lookup"><span data-stu-id="fa567-161">You can achieve the same result by using Certenroll.dll to create a new request object of the required type.</span></span>

## <a name="setpendingrequestinfowstr"></a><span data-ttu-id="fa567-162">сетпендингрекуестинфовстр</span><span class="sxs-lookup"><span data-stu-id="fa567-162">setPendingRequestInfoWStr</span></span>

<span data-ttu-id="fa567-163">Функция [**сетпендингрекуестинфовстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setpendingrequestinfowstr) в Xenroll.dll задает свойства ожидающего запроса.</span><span class="sxs-lookup"><span data-stu-id="fa567-163">The [**setPendingRequestInfoWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setpendingrequestinfowstr) function in Xenroll.dll specifies properties for the pending request.</span></span>

<span data-ttu-id="fa567-164">Библиотека CertEnroll.dll напрямую не реализует функции для удаления ожидающего запроса на сертификат.</span><span class="sxs-lookup"><span data-stu-id="fa567-164">The CertEnroll.dll library does not directly implement functionality to remove a pending certificate request.</span></span> <span data-ttu-id="fa567-165">Можно вызвать свойство [**каконфигстринг**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_caconfigstring) объекта [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , чтобы получить строку конфигурации, но только для активного объекта регистрации.</span><span class="sxs-lookup"><span data-stu-id="fa567-165">You can call the [**CAConfigString**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_caconfigstring) property on the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object to retrieve a configuration string but only for an active enrollment object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa567-166">См. также</span><span class="sxs-lookup"><span data-stu-id="fa567-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa567-167">Сопоставление Xenroll.dll CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="fa567-167">Mapping Xenroll.dll to CertEnroll.dll</span></span>](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[<span data-ttu-id="fa567-168">**исигнерцертификате**</span><span class="sxs-lookup"><span data-stu-id="fa567-168">**ISignerCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)
</dt> <dt>

[<span data-ttu-id="fa567-169">**IX509CertificateRequest**</span><span class="sxs-lookup"><span data-stu-id="fa567-169">**IX509CertificateRequest**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)
</dt> <dt>

[<span data-ttu-id="fa567-170">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="fa567-170">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[<span data-ttu-id="fa567-171">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="fa567-171">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[<span data-ttu-id="fa567-172">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="fa567-172">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[<span data-ttu-id="fa567-173">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="fa567-173">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> <dt>

[<span data-ttu-id="fa567-174">**IX509Enrollment**</span><span class="sxs-lookup"><span data-stu-id="fa567-174">**IX509Enrollment**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

