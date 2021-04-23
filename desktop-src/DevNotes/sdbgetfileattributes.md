---
description: Извлекает данные атрибута для указанного файла.
ms.assetid: 899b4af3-8185-4ce5-8e81-05ec3a446e42
title: Функция Сдбжетфилеаттрибутес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 651b9af34afdd2ffd767eba7ca4467ecfee081cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140735"
---
# <a name="sdbgetfileattributes-function"></a><span data-ttu-id="80631-103">Функция Сдбжетфилеаттрибутес</span><span class="sxs-lookup"><span data-stu-id="80631-103">SdbGetFileAttributes function</span></span>

<span data-ttu-id="80631-104">Извлекает данные атрибута для указанного файла.</span><span class="sxs-lookup"><span data-stu-id="80631-104">Retrieves the attribute data for the specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="80631-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80631-105">Syntax</span></span>


```C++
BOOL WINAPI SdbGetFileAttributes(
  _In_  LPCTSTR   lpwszFileName,
  _Out_ PATTRINFO *ppAttrInfo,
  _Out_ LPDWORD   lpdwAttrCount
);
```



## <a name="parameters"></a><span data-ttu-id="80631-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="80631-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80631-107">*лпвсзфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80631-107">*lpwszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80631-108">Путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="80631-108">The path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="80631-109">*ппаттринфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="80631-109">*ppAttrInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80631-110">Массив структур [**аттринфо**](attrinfo.md) , содержащих данные атрибута.</span><span class="sxs-lookup"><span data-stu-id="80631-110">An array of [**ATTRINFO**](attrinfo.md) structures that contain the attribute data.</span></span>

</dd> <dt>

<span data-ttu-id="80631-111">*лпдваттркаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="80631-111">*lpdwAttrCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80631-112">Количество атрибутов.</span><span class="sxs-lookup"><span data-stu-id="80631-112">The number of attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80631-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80631-113">Return value</span></span>

<span data-ttu-id="80631-114">Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="80631-114">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="80631-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80631-115">Remarks</span></span>

<span data-ttu-id="80631-116">Завершив работу с данными, освободите ее с помощью функции [**сдбфрифилеаттрибутес**](sdbfreefileattributes.md) .</span><span class="sxs-lookup"><span data-stu-id="80631-116">When you have finished with the data, free it using the [**SdbFreeFileAttributes**](sdbfreefileattributes.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="80631-117">Требования</span><span class="sxs-lookup"><span data-stu-id="80631-117">Requirements</span></span>



| <span data-ttu-id="80631-118">Требование</span><span class="sxs-lookup"><span data-stu-id="80631-118">Requirement</span></span> | <span data-ttu-id="80631-119">Значение</span><span class="sxs-lookup"><span data-stu-id="80631-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80631-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80631-120">Minimum supported client</span></span><br/> | <span data-ttu-id="80631-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80631-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="80631-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80631-122">Minimum supported server</span></span><br/> | <span data-ttu-id="80631-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="80631-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="80631-124">DLL</span><span class="sxs-lookup"><span data-stu-id="80631-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80631-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80631-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80631-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80631-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80631-127">**сдбформататтрибуте**</span><span class="sxs-lookup"><span data-stu-id="80631-127">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
</dt> <dt>

[<span data-ttu-id="80631-128">**сдбфрифилеаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="80631-128">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
</dt> </dl>

 

 




