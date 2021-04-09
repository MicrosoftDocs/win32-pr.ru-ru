---
title: Коды ошибок LDAP для ADSI
description: Когда сервер LDAP выдает ошибку и передает клиенту ошибку, эта ошибка затем преобразуется в строку клиентом LDAP.
ms.assetid: 7a0a5a1b-8473-405b-a590-3f917e50cbdc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149abf4562b0e35067149fb69c9a1ec1304cc528
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887520"
---
# <a name="ldap-error-codes-for-adsi"></a><span data-ttu-id="78424-103">Коды ошибок LDAP для ADSI</span><span class="sxs-lookup"><span data-stu-id="78424-103">LDAP Error Codes for ADSI</span></span>

<span data-ttu-id="78424-104">Когда сервер LDAP выдает ошибку и передает клиенту ошибку, эта ошибка затем преобразуется в строку клиентом LDAP.</span><span class="sxs-lookup"><span data-stu-id="78424-104">When an LDAP server generates an error and passes the error to the client, the error is then translated into a string by the LDAP client.</span></span>

<span data-ttu-id="78424-105">Этот метод аналогичен [кодам ошибок Win32 для ADSI](win32-error-codes-for-adsi.md).</span><span class="sxs-lookup"><span data-stu-id="78424-105">This method is similar to [Win32 error codes for ADSI](win32-error-codes-for-adsi.md).</span></span> <span data-ttu-id="78424-106">В этом примере код ошибки клиента — ошибка WIN32 0x80072020.</span><span class="sxs-lookup"><span data-stu-id="78424-106">In this example, the client error code is the WIN32 error 0x80072020.</span></span>

<span data-ttu-id="78424-107">**Определение кодов ошибок LDAP для ADSI**</span><span class="sxs-lookup"><span data-stu-id="78424-107">**To Determine the LDAP error codes for ADSI**</span></span>

1.  <span data-ttu-id="78424-108">Удалите 8007 из кода ошибки WIN32.</span><span class="sxs-lookup"><span data-stu-id="78424-108">Drop the 8007 from the WIN32 error code.</span></span> <span data-ttu-id="78424-109">В этом примере оставшееся шестнадцатеричное значение — 2020.</span><span class="sxs-lookup"><span data-stu-id="78424-109">In the example, the remaining hex value is 2020.</span></span>
2.  <span data-ttu-id="78424-110">Преобразуйте оставшееся шестнадцатеричное значение в десятичное.</span><span class="sxs-lookup"><span data-stu-id="78424-110">Convert the remaining hex value to a decimal value.</span></span> <span data-ttu-id="78424-111">В этом примере оставшееся шестнадцатеричное значение 2020 преобразуется в десятичное значение 8224.</span><span class="sxs-lookup"><span data-stu-id="78424-111">In the example, the remaining hex value 2020 converts to the decimal value 8224.</span></span>
3.  <span data-ttu-id="78424-112">Найдите в файле WinError. h определение десятичного значения.</span><span class="sxs-lookup"><span data-stu-id="78424-112">Search in the WinError.h file for the definition of the decimal value.</span></span> <span data-ttu-id="78424-113">В этом примере 8224L соответствует ошибке **\_ Operations Error DS \_ \_ Error**.</span><span class="sxs-lookup"><span data-stu-id="78424-113">In the example, 8224L corresponds to the error **ERROR\_DS\_OPERATIONS\_ERROR**.</span></span>
4.  <span data-ttu-id="78424-114">Замените префикс **Errors \_ DS** на **LDAP \_**.</span><span class="sxs-lookup"><span data-stu-id="78424-114">Replace the prefix **ERROR\_DS** with **LDAP\_**.</span></span> <span data-ttu-id="78424-115">В этом примере новое определение — **\_ \_ Ошибка операций LDAP**.</span><span class="sxs-lookup"><span data-stu-id="78424-115">In the example, the new definition is **LDAP\_OPERATIONS\_ERROR**.</span></span>
5.  <span data-ttu-id="78424-116">Найдите в файле Винлдап. h значение определения ошибки LDAP.</span><span class="sxs-lookup"><span data-stu-id="78424-116">Search in the Winldap.h file for the value of the LDAP error definition.</span></span> <span data-ttu-id="78424-117">В этом примере значение **\_ \_ ошибки операций LDAP** в файле винлдап. h — 0x01.</span><span class="sxs-lookup"><span data-stu-id="78424-117">In the example, the value of **LDAP\_OPERATIONS\_ERROR** in the Winldap.h file is 0x01.</span></span>

 

 




