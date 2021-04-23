---
description: Добавляет альтернативное имя локальной сети для компьютера, с которого он вызывается.
ms.assetid: e4d8355b-0492-4b6f-988f-3887e63a2bba
title: Функция Аддлокалалтернатекомпутернаме
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddLocalAlternateComputerName
- AddLocalAlternateComputerNameA
- AddLocalAlternateComputerNameW
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
- kernel32legacy.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
- API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
ms.openlocfilehash: 6027752a0e60f135f0cc8a1c0cdd536c59c09621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648925"
---
# <a name="addlocalalternatecomputername-function"></a><span data-ttu-id="9c9ac-103">Функция Аддлокалалтернатекомпутернаме</span><span class="sxs-lookup"><span data-stu-id="9c9ac-103">AddLocalAlternateComputerName function</span></span>

<span data-ttu-id="9c9ac-104">Добавляет альтернативное имя локальной сети для компьютера, с которого он вызывается.</span><span class="sxs-lookup"><span data-stu-id="9c9ac-104">Adds an alternate local network name for the computer from which it is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c9ac-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c9ac-105">Syntax</span></span>


```C++
DWORD AddLocalAlternateComputerName(
  _In_ LPCTSTR lpDnsFQHostname,
  _In_ ULONG   ulFlags
);
```



## <a name="parameters"></a><span data-ttu-id="9c9ac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c9ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c9ac-107">*лпднсфкхостнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c9ac-107">*lpDnsFQHostname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c9ac-108">Добавляемое альтернативное имя.</span><span class="sxs-lookup"><span data-stu-id="9c9ac-108">The alternate name to be added.</span></span> <span data-ttu-id="9c9ac-109">Имя должно быть в формате **компутернамеднсфулликуалифиед** , как определено в перечислении [**\_ \_ форматов имен компьютеров**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) , а функция [**днсвалидатенаме \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) должна иметь возможность проверить ее, указав для ее формата значение **днснамехостнамефулл**.</span><span class="sxs-lookup"><span data-stu-id="9c9ac-109">The name must be in the **ComputerNameDnsFullyQualified** format as defined in the [**COMPUTER\_NAME\_FORMAT**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) enumeration, and the [**DnsValidateName\_W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) function must be able to validate it with its format set to **DnsNameHostnameFull**.</span></span>

</dd> <dt>

<span data-ttu-id="9c9ac-110">*улфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c9ac-110">*ulFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c9ac-111">Этот параметр зарезервирован и должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="9c9ac-111">This parameter is reserved and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c9ac-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c9ac-112">Return value</span></span>

<span data-ttu-id="9c9ac-113">Если функция завершается успешно, функция возвращает **ошибку \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="9c9ac-113">If the function succeeds, the function returns **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="9c9ac-114">Если функция завершается ошибкой, она возвращает ненулевой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="9c9ac-114">If the function fails, it returns a nonzero error code.</span></span> <span data-ttu-id="9c9ac-115">К возвращенным им кодам ошибок относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="9c9ac-115">Among the error codes that it returns are the following:</span></span>



| <span data-ttu-id="9c9ac-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9c9ac-116">Return code</span></span>                                                                                               | <span data-ttu-id="9c9ac-117">Описание</span><span class="sxs-lookup"><span data-stu-id="9c9ac-117">Description</span></span>                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9c9ac-118"><dt>**Ошибка \_ недопустимого \_ параметра**</dt></span><span class="sxs-lookup"><span data-stu-id="9c9ac-118"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>  | <span data-ttu-id="9c9ac-119">Указывает, что параметр *лпднсфкхостнаме* не указывает на допустимое DNS-имя или что параметр *улфлагс* не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="9c9ac-119">Indicates that the *lpDnsFQHostname* parameter does not point to a valid DNS name, or that the *ulFlags* parameter is not equal to zero.</span></span><br/> |
| <dl> <span data-ttu-id="9c9ac-120"><dt>**Ошибка \_ не \_ хватает \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="9c9ac-120"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="9c9ac-121">Недостаточно памяти для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="9c9ac-121">There is not enough memory to complete the operation.</span></span><br/>                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="9c9ac-122">Требования</span><span class="sxs-lookup"><span data-stu-id="9c9ac-122">Requirements</span></span>



| <span data-ttu-id="9c9ac-123">Требование</span><span class="sxs-lookup"><span data-stu-id="9c9ac-123">Requirement</span></span> | <span data-ttu-id="9c9ac-124">Значение</span><span class="sxs-lookup"><span data-stu-id="9c9ac-124">Value</span></span> |
|-----------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c9ac-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9c9ac-125">Library</span></span><br/>                | <dl> <span data-ttu-id="9c9ac-126"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c9ac-126"><dt>Kernel32.lib</dt></span></span> </dl>               |
| <span data-ttu-id="9c9ac-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9c9ac-127">DLL</span></span><br/>                    | <dl> <span data-ttu-id="9c9ac-128"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c9ac-128"><dt>Kernel32.dll</dt></span></span> </dl>               |
| <span data-ttu-id="9c9ac-129">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="9c9ac-129">Unicode and ANSI names</span></span><br/> | <span data-ttu-id="9c9ac-130">**Аддлокалалтернатекомпутернамев** (Юникод) и **аддлокалалтернатекомпутернамеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9c9ac-130">**AddLocalAlternateComputerNameW** (Unicode) and **AddLocalAlternateComputerNameA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9c9ac-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c9ac-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c9ac-132">**\_Формат имени \_ компьютера**</span><span class="sxs-lookup"><span data-stu-id="9c9ac-132">**COMPUTER\_NAME\_FORMAT**</span></span>](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format)
</dt> <dt>

[<span data-ttu-id="9c9ac-133">**Днсвалидатенаме \_ W**</span><span class="sxs-lookup"><span data-stu-id="9c9ac-133">**DnsValidateName\_W**</span></span>](/windows/win32/api/windns/nf-windns-dnsvalidatename)
</dt> </dl>

 

 
