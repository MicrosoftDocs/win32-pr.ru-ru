---
title: Коды ошибок Win32 для ADSI
description: Стандартные коды ошибок Win32 также используются для возврата сообщений об ошибках ADSI.
ms.assetid: 5b7b85c9-ccca-4ea3-8b37-54f6b30a509f
ms.tgt_platform: multiple
keywords:
- Коды ошибок Win32 для ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a47151a3a1619a7f224dc0b9b7f0871813a346a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772884"
---
# <a name="win32-error-codes-for-adsi"></a><span data-ttu-id="13be0-104">Коды ошибок Win32 для ADSI</span><span class="sxs-lookup"><span data-stu-id="13be0-104">Win32 Error Codes for ADSI</span></span>

<span data-ttu-id="13be0-105">Стандартные коды ошибок Win32 также используются для возврата сообщений об ошибках ADSI.</span><span class="sxs-lookup"><span data-stu-id="13be0-105">Standard Win32 error codes are also used to return ADSI error messages.</span></span> <span data-ttu-id="13be0-106">В частности, поставщик LDAP ADSI сопоставляет все коды ошибок LDAP с кодами ошибок Win32.</span><span class="sxs-lookup"><span data-stu-id="13be0-106">Specifically, the ADSI LDAP provider maps all the LDAP error codes to Win32 error codes.</span></span> <span data-ttu-id="13be0-107">Значения **HRESULT** этих кодов ошибок имеют формат 0x8007XXXX, где четыре последние шестнадцатеричные цифры (xxxx) соответствуют значениям **DWORD** соответствующего кода ошибки Win32.</span><span class="sxs-lookup"><span data-stu-id="13be0-107">The **HRESULT** values of these error codes are of the 0x8007XXXX format, where the last four hexadecimal digits, XXXX, corresponds to the **DWORD** values of the appropriate Win32 error code.</span></span> <span data-ttu-id="13be0-108">Например, значение ошибки ADSI 0x80072020 дает значение ошибки Win32 0x2020 в шестнадцатеричном или 8224 в десятичном формате.</span><span class="sxs-lookup"><span data-stu-id="13be0-108">For example, the ADSI error value 0x80072020 gives the Win32 error value of 0x2020 in hexadecimal or 8224 in decimal.</span></span>

<span data-ttu-id="13be0-109">Чтобы преобразовать значение **HRESULT** кода ошибки ADSI, возвращенного приложением, в соответствующее значение **DWORD** ошибки Win32, как определено в заголовочных файлах выше, используйте следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="13be0-109">To convert the **HRESULT** value of an ADSI error code, returned by your application, to the corresponding the Win32 error **DWORD** value, as defined in the header files above, use the following procedure.</span></span>

<span data-ttu-id="13be0-110">Большинство кодов ошибок Win32 для ADSI определены в файле Winerror. h или Лмерр. h.</span><span class="sxs-lookup"><span data-stu-id="13be0-110">Most of the Win32 error codes for ADSI are defined in Winerror.h or Lmerr.h.</span></span> <span data-ttu-id="13be0-111">Значения ошибок перечислены в виде десятичных значений в этих файлах.</span><span class="sxs-lookup"><span data-stu-id="13be0-111">The error values are listed as decimal values in these files.</span></span>

<span data-ttu-id="13be0-112">**Преобразование значения **HRESULT** кода ошибки ADSI в соответствующее значение **DWORD** ошибки Win32**</span><span class="sxs-lookup"><span data-stu-id="13be0-112">**To convert the **HRESULT** value of an ADSI error code to the corresponding the Win32 error **DWORD** value**</span></span>

1.  <span data-ttu-id="13be0-113">Преобразуйте значение **HRESULT** в шестнадцатеричное число, если оно начинается с десятичного значения, как вы можете получить из Visual Basic приложения.</span><span class="sxs-lookup"><span data-stu-id="13be0-113">Convert the **HRESULT** value to a hexadecimal number if starting with a decimal value as you may get from a Visual Basic application.</span></span>
2.  <span data-ttu-id="13be0-114">Удалите часть 0x8007, чтобы получить остаток.</span><span class="sxs-lookup"><span data-stu-id="13be0-114">Drop the 0x8007 part produce the remainder.</span></span>
3.  <span data-ttu-id="13be0-115">Преобразуйте остаток в десятичное число.</span><span class="sxs-lookup"><span data-stu-id="13be0-115">Convert the remainder to a decimal number.</span></span>
4.  <span data-ttu-id="13be0-116">Поиск десятичного остатка в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="13be0-116">Look up the decimal remainder in Winerror.h.</span></span>
5.  <span data-ttu-id="13be0-117">Если не найдено в файле Winerror. h, вычтите 2100 из десятичного остатка и найдите результат в Лмерр. h.</span><span class="sxs-lookup"><span data-stu-id="13be0-117">If not found in Winerror.h, subtract 2100 from the decimal remainder and look up the result in Lmerr.h.</span></span>

<span data-ttu-id="13be0-118">ADSI 2,0 сопоставляет коды ошибок LDAP набору кодов ошибок Win32, отличающихся от тех, которые использовались в ADSI для Windows 2000 и клиента DS.</span><span class="sxs-lookup"><span data-stu-id="13be0-118">ADSI 2.0 maps the LDAP error codes to a set of Win32 error codes that is different from that used in ADSI for Windows 2000 and DS Client.</span></span> <span data-ttu-id="13be0-119">Различия перечислены в:</span><span class="sxs-lookup"><span data-stu-id="13be0-119">The differences are listed in:</span></span>

-   [<span data-ttu-id="13be0-120">Коды ошибок Win32</span><span class="sxs-lookup"><span data-stu-id="13be0-120">Win32 Error Codes</span></span>](win32-error-codes.md)
-   [<span data-ttu-id="13be0-121">Коды ошибок Win32 для ADSI 2,0</span><span class="sxs-lookup"><span data-stu-id="13be0-121">Win32 Error Codes for ADSI 2.0</span></span>](win32-error-codes-for-adsi-2-0.md)

 

 




