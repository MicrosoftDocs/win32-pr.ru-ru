---
description: В каждом из следующих разделов обсуждается функция, экспортируемая с помощью Xenroll.dll. В каждом разделе также обсуждается использование CertEnroll.dll для замены функции или указывает, что сопоставление между двумя библиотеками не существует.
ms.assetid: 06d8dd6f-7a8d-4da5-a99d-9c9d8fb90cfa
title: Вспомогательные функции (API регистрации сертификатов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ee272e7b11c3fccf7975c5356302a2961b32ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347745"
---
# <a name="helper-functions-certificate-enrollment-api"></a><span data-ttu-id="75794-104">Вспомогательные функции (API регистрации сертификатов)</span><span class="sxs-lookup"><span data-stu-id="75794-104">Helper Functions (Certificate Enrollment API)</span></span>

<span data-ttu-id="75794-105">В каждом из следующих разделов обсуждается функция, экспортируемая с помощью Xenroll.dll.</span><span class="sxs-lookup"><span data-stu-id="75794-105">Each of the following sections discusses a function exported by Xenroll.dll.</span></span> <span data-ttu-id="75794-106">В каждом разделе также обсуждается использование CertEnroll.dll для замены функции или указывает, что сопоставление между двумя библиотеками не существует.</span><span class="sxs-lookup"><span data-stu-id="75794-106">Each section also discusses how to use CertEnroll.dll to replace the function or indicates that no mapping between the two libraries exists.</span></span>

## <a name="binaryblobtostring"></a><span data-ttu-id="75794-107">бинариблобтостринг</span><span class="sxs-lookup"><span data-stu-id="75794-107">binaryBlobToString</span></span>

<span data-ttu-id="75794-108">Функция [**бинариблобтостринг**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) в Xenroll.dll преобразует массив байтов в строку.</span><span class="sxs-lookup"><span data-stu-id="75794-108">The [**binaryBlobToString**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) function in Xenroll.dll converts a byte array to a string.</span></span>

<span data-ttu-id="75794-109">С помощью CertEnroll.dll можно вызвать метод [**вариантбитеаррайтостринг**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring) в интерфейсе [**ибинариконвертер**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) .</span><span class="sxs-lookup"><span data-stu-id="75794-109">Using CertEnroll.dll, you can call the [**VariantByteArrayToString**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring) method on the [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) interface.</span></span>

## <a name="stringtobinaryblob"></a><span data-ttu-id="75794-110">стрингтобинариблоб</span><span class="sxs-lookup"><span data-stu-id="75794-110">stringToBinaryBlob</span></span>

<span data-ttu-id="75794-111">Функция [**стрингтобинариблоб**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) в Xenroll.dll преобразует строку в массив байтов.</span><span class="sxs-lookup"><span data-stu-id="75794-111">The [**stringToBinaryBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) function in Xenroll.dll converts a string to a byte array.</span></span>

<span data-ttu-id="75794-112">С помощью CertEnroll.dll можно вызвать метод [**стрингтовариантбитеаррай**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray) в интерфейсе [**ибинариконвертер**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) .</span><span class="sxs-lookup"><span data-stu-id="75794-112">Using CertEnroll.dll, you can call the [**StringToVariantByteArray**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray) method on the [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75794-113">См. также</span><span class="sxs-lookup"><span data-stu-id="75794-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75794-114">Сопоставление Xenroll.dll CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="75794-114">Mapping Xenroll.dll to CertEnroll.dll</span></span>](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[<span data-ttu-id="75794-115">**ибинариконвертер**</span><span class="sxs-lookup"><span data-stu-id="75794-115">**IBinaryConverter**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)
</dt> </dl>

 

 
