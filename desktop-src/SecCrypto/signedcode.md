---
description: Предоставляет функциональные возможности для подписывания исполняемых файлов с помощью цифровой подписи Authenticode.
ms.assetid: e6d4e694-471f-4d30-983c-6bc5d631d99e
title: Объект Сигнедкоде
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 08648c8b941874a6d1e1ed97d49f510694b998b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669314"
---
# <a name="signedcode-object"></a><span data-ttu-id="b84b1-103">Объект Сигнедкоде</span><span class="sxs-lookup"><span data-stu-id="b84b1-103">SignedCode object</span></span>

<span data-ttu-id="b84b1-104">\[Объект **сигнедкоде** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="b84b1-104">\[The **SignedCode** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b84b1-105">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций Win32 API [**сигнерсигнекс**](signersignex.md), [**сигнертиместампекс**](signertimestampex.md)и [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) для подписи содержимого цифровой подписью Authenticode.</span><span class="sxs-lookup"><span data-stu-id="b84b1-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="b84b1-106">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="b84b1-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="b84b1-107">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="b84b1-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="b84b1-108">Объект **сигнедкоде** предоставляет функциональные возможности для подписывания исполняемых файлов с помощью цифровой подписи Authenticode.</span><span class="sxs-lookup"><span data-stu-id="b84b1-108">The **SignedCode** object provides functionality for signing executable files with an Authenticode digital signature.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="b84b1-109">Назначение</span><span class="sxs-lookup"><span data-stu-id="b84b1-109">When to use</span></span>

<span data-ttu-id="b84b1-110">Объект **сигнедкоде** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="b84b1-110">The **SignedCode** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="b84b1-111">Подписывать исполняемые файлы.</span><span class="sxs-lookup"><span data-stu-id="b84b1-111">Sign executable files.</span></span>
-   <span data-ttu-id="b84b1-112">Исполняемые файлы меток времени.</span><span class="sxs-lookup"><span data-stu-id="b84b1-112">Time stamp executable files.</span></span>
-   <span data-ttu-id="b84b1-113">Определить, является ли подпись исполняемого файла допустимой.</span><span class="sxs-lookup"><span data-stu-id="b84b1-113">Determine whether the signature of the executable file is valid.</span></span>
-   <span data-ttu-id="b84b1-114">Задайте или получите путь к исполняемому файлу.</span><span class="sxs-lookup"><span data-stu-id="b84b1-114">Set or retrieve the path to the executable file.</span></span>
-   <span data-ttu-id="b84b1-115">Получите подписывающий и Time Стампер исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="b84b1-115">Retrieve the signer and time stamper of the executable file.</span></span>
-   <span data-ttu-id="b84b1-116">Получение коллекции сертификатов для исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="b84b1-116">Retrieve a collection of the certificates for the executable file.</span></span>
-   <span data-ttu-id="b84b1-117">Получите описание или URL-адрес для описания исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="b84b1-117">Retrieve a description or the URL to the description of the executable file.</span></span>

## <a name="members"></a><span data-ttu-id="b84b1-118">Элементы</span><span class="sxs-lookup"><span data-stu-id="b84b1-118">Members</span></span>

<span data-ttu-id="b84b1-119">Объект **сигнедкоде** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b84b1-119">The **SignedCode** object has these types of members:</span></span>

-   [<span data-ttu-id="b84b1-120">Методы</span><span class="sxs-lookup"><span data-stu-id="b84b1-120">Methods</span></span>](#methods)
-   [<span data-ttu-id="b84b1-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="b84b1-121">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b84b1-122">Методы</span><span class="sxs-lookup"><span data-stu-id="b84b1-122">Methods</span></span>

<span data-ttu-id="b84b1-123">Объект **сигнедкоде** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="b84b1-123">The **SignedCode** object has these methods.</span></span>



| <span data-ttu-id="b84b1-124">Метод</span><span class="sxs-lookup"><span data-stu-id="b84b1-124">Method</span></span>                                    | <span data-ttu-id="b84b1-125">Описание</span><span class="sxs-lookup"><span data-stu-id="b84b1-125">Description</span></span>                                                                                                                                                         |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b84b1-126">**Писать**</span><span class="sxs-lookup"><span data-stu-id="b84b1-126">**Sign**</span></span>](signedcode-sign.md)           | <span data-ttu-id="b84b1-127">Создает цифровую подпись Authenticode и подписывает исполняемый файл, указанный в свойстве [**сигнедкоде. filename**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="b84b1-127">Creates an Authenticode digital signature and signs the executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/>    |
| [<span data-ttu-id="b84b1-128">**Отметка времени**</span><span class="sxs-lookup"><span data-stu-id="b84b1-128">**Timestamp**</span></span>](signedcode-timestamp.md) | <span data-ttu-id="b84b1-129">Создает подпись метки времени Authenticode для подписанного исполняемого файла, указанного в свойстве [**сигнедкоде. filename**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="b84b1-129">Creates an Authenticode time stamp signature on the signed executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/> |
| [<span data-ttu-id="b84b1-130">**Проверка**</span><span class="sxs-lookup"><span data-stu-id="b84b1-130">**Verify**</span></span>](signedcode-verify.md)       | <span data-ttu-id="b84b1-131">Проверяет подпись Authenticode для подписанного исполняемого файла, указанного в свойстве [**сигнедкоде. filename**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="b84b1-131">Verifies the Authenticode signature on the signed executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="b84b1-132">Свойства</span><span class="sxs-lookup"><span data-stu-id="b84b1-132">Properties</span></span>

<span data-ttu-id="b84b1-133">Объект **сигнедкоде** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b84b1-133">The **SignedCode** object has these properties.</span></span>



| <span data-ttu-id="b84b1-134">Свойство</span><span class="sxs-lookup"><span data-stu-id="b84b1-134">Property</span></span>                                                       | <span data-ttu-id="b84b1-135">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="b84b1-135">Access type</span></span>           | <span data-ttu-id="b84b1-136">Описание</span><span class="sxs-lookup"><span data-stu-id="b84b1-136">Description</span></span>                                                                                                                                |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b84b1-137">**Сертификаты**</span><span class="sxs-lookup"><span data-stu-id="b84b1-137">**Certificates**</span></span>](signedcode-certificates.md)<br/>     | <span data-ttu-id="b84b1-138">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b84b1-138">Read-only</span></span><br/>  | <span data-ttu-id="b84b1-139">Коллекция [**сертификатов**](certificates.md) , которая содержит все сертификаты в подписанном исполняемом файле.</span><span class="sxs-lookup"><span data-stu-id="b84b1-139">A [**Certificates**](certificates.md) collection that contains all the certificates in the signed executable file.</span></span><br/>             |
| [<span data-ttu-id="b84b1-140">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b84b1-140">**Description**</span></span>](signedcode-description.md)<br/>       | <span data-ttu-id="b84b1-141">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="b84b1-141">Read/write</span></span><br/> | <span data-ttu-id="b84b1-142">Строка, содержащая описание подписанного исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="b84b1-142">A string that contains a description of the signed executable file.</span></span><br/>                                                             |
| [<span data-ttu-id="b84b1-143">**дескриптионурл**</span><span class="sxs-lookup"><span data-stu-id="b84b1-143">**DescriptionURL**</span></span>](signedcode-descriptionurl.md)<br/> | <span data-ttu-id="b84b1-144">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="b84b1-144">Read/write</span></span><br/> | <span data-ttu-id="b84b1-145">Строка, содержащая HTTP-адрес для описания подписанного исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="b84b1-145">A string that contains the HTTP address to a description of the signed executable file.</span></span><br/>                                         |
| [<span data-ttu-id="b84b1-146">**Файлов**</span><span class="sxs-lookup"><span data-stu-id="b84b1-146">**FileName**</span></span>](signedcode-filename.md)<br/>             | <span data-ttu-id="b84b1-147">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="b84b1-147">Read/write</span></span><br/> | <span data-ttu-id="b84b1-148">Строка, содержащая путь к файлу содержимого, содержащему исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="b84b1-148">A string that contains the path to the content file that contains the executable file.</span></span><br/> <span data-ttu-id="b84b1-149">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b84b1-149">This is the default property.</span></span><br/> |
| [<span data-ttu-id="b84b1-150">**Автор подписи**</span><span class="sxs-lookup"><span data-stu-id="b84b1-150">**Signer**</span></span>](signedcode-signer.md)<br/>                 | <span data-ttu-id="b84b1-151">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b84b1-151">Read-only</span></span><br/>  | <span data-ttu-id="b84b1-152">Объект- [**подписавший**](signer.md) , который предоставляет доступ к подписывания исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="b84b1-152">A [**Signer**](signer.md) object that provides access to the signer of the executable file.</span></span><br/>                                    |
| [<span data-ttu-id="b84b1-153">**Timestamper**</span><span class="sxs-lookup"><span data-stu-id="b84b1-153">**Timestamper**</span></span>](signedcode-timestamper.md)<br/>       | <span data-ttu-id="b84b1-154">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b84b1-154">Read-only</span></span><br/>  | <span data-ttu-id="b84b1-155">Объект- [**подписавший**](signer.md) , предоставляющий доступ к времени Стампер исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="b84b1-155">A [**Signer**](signer.md) object that provides access to the time stamper of the executable file.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="b84b1-156">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b84b1-156">Remarks</span></span>

<span data-ttu-id="b84b1-157">Объект **сигнедкоде** может быть создан и незащищен для создания скриптов.</span><span class="sxs-lookup"><span data-stu-id="b84b1-157">The **SignedCode** object can be created, and is not safe for scripting.</span></span> <span data-ttu-id="b84b1-158">ProgID для объекта **сигнедкоде** — CAPICOM. Сигнедкоде. 1.</span><span class="sxs-lookup"><span data-stu-id="b84b1-158">The ProgID for the **SignedCode** object is CAPICOM.SignedCode.1.</span></span>

<span data-ttu-id="b84b1-159">Исполняемый файл должен иметь тип, который может быть подписан с помощью технологии Authenticode, например файлы с расширением. cab,. cat,. exe,. dll,. vbs или. ocx.</span><span class="sxs-lookup"><span data-stu-id="b84b1-159">The executable file should be of a type that can be signed with Authenticode technology, for example, files that have a file name extension of .cab, .cat, .exe, .dll, .vbs, or .ocx.</span></span>

## <a name="requirements"></a><span data-ttu-id="b84b1-160">Требования</span><span class="sxs-lookup"><span data-stu-id="b84b1-160">Requirements</span></span>



| <span data-ttu-id="b84b1-161">Требование</span><span class="sxs-lookup"><span data-stu-id="b84b1-161">Requirement</span></span> | <span data-ttu-id="b84b1-162">Значение</span><span class="sxs-lookup"><span data-stu-id="b84b1-162">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b84b1-163">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="b84b1-163">Redistributable</span></span><br/> | <span data-ttu-id="b84b1-164">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="b84b1-164">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b84b1-165">DLL</span><span class="sxs-lookup"><span data-stu-id="b84b1-165">DLL</span></span><br/>             | <dl> <span data-ttu-id="b84b1-166"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b84b1-166"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
