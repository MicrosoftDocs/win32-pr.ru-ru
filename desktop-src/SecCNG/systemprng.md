---
description: Извлекает указанное число случайных байтов из системного генератора случайных чисел.
ms.assetid: 04746229-9dc1-4748-80c1-f1960bd1b768
title: Функция SystemPrng
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemPrng
api_type:
- DllExport
api_location:
- Ksecdd.sys
- Cng.sys
ms.openlocfilehash: d847d34ffd11e158170f55599de0ceb3acf3c697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662331"
---
# <a name="systemprng-function"></a><span data-ttu-id="839a5-103">Функция SystemPrng</span><span class="sxs-lookup"><span data-stu-id="839a5-103">SystemPrng function</span></span>

<span data-ttu-id="839a5-104">\[**SystemPrng** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="839a5-104">\[**SystemPrng** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="839a5-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="839a5-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="839a5-106">Вместо этого используйте [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]</span><span class="sxs-lookup"><span data-stu-id="839a5-106">Instead, use [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]</span></span>

<span data-ttu-id="839a5-107">Функция **SystemPrng** извлекает указанное число случайных байтов из системного генератора случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="839a5-107">The **SystemPrng** function retrieves a specified number of random bytes from the system random number generator.</span></span>

> [!Note]  
> <span data-ttu-id="839a5-108">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="839a5-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="839a5-109">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем.</span><span class="sxs-lookup"><span data-stu-id="839a5-109">To call this function, you must create a user-defined header file.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="839a5-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="839a5-110">Syntax</span></span>


```C++
BOOL SystemPrng(
  _Out_ unsigned char pbRandomData,
  _In_  size_t        cbRandomData
);
```



## <a name="parameters"></a><span data-ttu-id="839a5-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="839a5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="839a5-112">*пбрандомдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="839a5-112">*pbRandomData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="839a5-113">Указатель на буфер, который получает извлеченные байты.</span><span class="sxs-lookup"><span data-stu-id="839a5-113">A pointer to a buffer that receives the retrieved bytes.</span></span>

</dd> <dt>

<span data-ttu-id="839a5-114">*кбрандомдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="839a5-114">*cbRandomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="839a5-115">Число извлекаемых байтов.</span><span class="sxs-lookup"><span data-stu-id="839a5-115">The number of bytes to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="839a5-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="839a5-116">Return value</span></span>

<span data-ttu-id="839a5-117">Всегда возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="839a5-117">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="839a5-118">Требования</span><span class="sxs-lookup"><span data-stu-id="839a5-118">Requirements</span></span>



| <span data-ttu-id="839a5-119">Требование</span><span class="sxs-lookup"><span data-stu-id="839a5-119">Requirement</span></span> | <span data-ttu-id="839a5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="839a5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="839a5-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="839a5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="839a5-122">Только для настольных приложений Windows Vista с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="839a5-122">Windows Vista with SP1 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                        |
| <span data-ttu-id="839a5-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="839a5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="839a5-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="839a5-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                           |
| <span data-ttu-id="839a5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="839a5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="839a5-126"><dt>Ksecdd.sys в Windows Server 2008 и Windows Vista с пакетом обновления 1 (SP1); </dt> <dt>Cng.sys в Windows 7 и Windows Server 2008 R2</dt></span><span class="sxs-lookup"><span data-stu-id="839a5-126"><dt>Ksecdd.sys on Windows Server 2008 and Windows Vista with SP1; </dt> <dt>Cng.sys on Windows 7 and Windows Server 2008 R2</dt></span></span> </dl> |



 

 




