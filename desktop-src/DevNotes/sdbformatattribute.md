---
description: Преобразует указанные данные атрибута в формат XML.
ms.assetid: 7a75726d-f1ec-4137-89c1-eccb4a78fc22
title: Функция Сдбформататтрибуте
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFormatAttribute
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e06bbaa288c7ecb0e85cd8a779100d547c33d687
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895253"
---
# <a name="sdbformatattribute-function"></a><span data-ttu-id="493ec-103">Функция Сдбформататтрибуте</span><span class="sxs-lookup"><span data-stu-id="493ec-103">SdbFormatAttribute function</span></span>

<span data-ttu-id="493ec-104">Преобразует указанные данные атрибута в формат XML.</span><span class="sxs-lookup"><span data-stu-id="493ec-104">Converts the specified attribute data to XML format.</span></span>

## <a name="syntax"></a><span data-ttu-id="493ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="493ec-105">Syntax</span></span>


```C++
BOOL WINAPI SdbFormatAttribute(
  _In_  PATTRINFO pAttrInfo,
  _Out_ LPTSTR    pchBuffer,
  _In_  DWORD     dwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="493ec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="493ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="493ec-107">*паттринфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="493ec-107">*pAttrInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="493ec-108">Структура [**аттринфо**](attrinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="493ec-108">An [**ATTRINFO**](attrinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="493ec-109">*пчбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="493ec-109">*pchBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="493ec-110">Выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="493ec-110">The output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="493ec-111">*двбуфферсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="493ec-111">*dwBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="493ec-112">Размер буфера *пчбуффер* в символах.</span><span class="sxs-lookup"><span data-stu-id="493ec-112">The size of the *pchBuffer* buffer, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="493ec-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="493ec-113">Return value</span></span>

<span data-ttu-id="493ec-114">Функция возвращает **значение true** при успешном выполнении или **значение false** , если буфер слишком мал или не найден атрибут.</span><span class="sxs-lookup"><span data-stu-id="493ec-114">The function returns **TRUE** on success or **FALSE** if the buffer is too small or the attribute is not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="493ec-115">Требования</span><span class="sxs-lookup"><span data-stu-id="493ec-115">Requirements</span></span>



| <span data-ttu-id="493ec-116">Требование</span><span class="sxs-lookup"><span data-stu-id="493ec-116">Requirement</span></span> | <span data-ttu-id="493ec-117">Значение</span><span class="sxs-lookup"><span data-stu-id="493ec-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="493ec-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="493ec-118">Minimum supported client</span></span><br/> | <span data-ttu-id="493ec-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="493ec-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="493ec-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="493ec-120">Minimum supported server</span></span><br/> | <span data-ttu-id="493ec-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="493ec-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="493ec-122">DLL</span><span class="sxs-lookup"><span data-stu-id="493ec-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="493ec-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="493ec-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="493ec-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="493ec-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="493ec-125">**сдбжетфилеаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="493ec-125">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 




