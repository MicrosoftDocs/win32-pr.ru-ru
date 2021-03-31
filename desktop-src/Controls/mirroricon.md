---
title: Функция Миррорикон
description: Меняет местами значки (зеркала), чтобы они отображались правильно в контексте зеркального устройства.
ms.assetid: bca87037-1789-466b-9be0-914966fdad31
keywords:
- Элементы управления Windows для функций Миррорикон
topic_type:
- apiref
api_name:
- MirrorIcon
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02f180d509464b63e5ec73c5fb74e4d70386bdea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071253"
---
# <a name="mirroricon-function"></a><span data-ttu-id="6be62-104">Функция Миррорикон</span><span class="sxs-lookup"><span data-stu-id="6be62-104">MirrorIcon function</span></span>

<span data-ttu-id="6be62-105">\[**Миррорикон** доступен в Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="6be62-105">\[**MirrorIcon** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="6be62-106">Он может быть изменен или недоступен в последующих версиях.\]</span><span class="sxs-lookup"><span data-stu-id="6be62-106">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="6be62-107">Меняет местами значки (зеркала), чтобы они отображались правильно в контексте зеркального устройства.</span><span class="sxs-lookup"><span data-stu-id="6be62-107">Reverses (mirrors) icons so that they are displayed correctly on a mirrored device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="6be62-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6be62-108">Syntax</span></span>


```C++
BOOL WINAPI MirrorIcon(
  _Inout_opt_ HICON *phIconSmall,
  _Inout_opt_ HICON *phIconLarge
);
```



## <a name="parameters"></a><span data-ttu-id="6be62-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6be62-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6be62-110">*фиконсмалл* \[ в, out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="6be62-110">*phIconSmall* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6be62-111">Тип: \**[**Хикон**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="6be62-111">Type: \**[**HICON**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="6be62-112">Указатель на маркер значка, который ссылается на небольшую версию значка.</span><span class="sxs-lookup"><span data-stu-id="6be62-112">A pointer to the icon handle that references a small version of an icon.</span></span>

</dd> <dt>

<span data-ttu-id="6be62-113">_phIconLarge \* \[ в, out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="6be62-113">_phIconLarge\* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6be62-114">Тип: \**[**Хикон**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="6be62-114">Type: \**[**HICON**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="6be62-115">Указатель на маркер значка, который ссылается на крупную версию значка.</span><span class="sxs-lookup"><span data-stu-id="6be62-115">A pointer to the icon handle that references a large version of an icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6be62-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6be62-116">Return value</span></span>

<span data-ttu-id="6be62-117">Тип: _ *[**bool**](/windows/desktop/WinProg/windows-data-types)*\*</span><span class="sxs-lookup"><span data-stu-id="6be62-117">Type: _ *[**BOOL**](/windows/desktop/WinProg/windows-data-types)*\*</span></span>

<span data-ttu-id="6be62-118">**Значение true** в случае успешного выполнения; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="6be62-118">**TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6be62-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6be62-119">Remarks</span></span>

<span data-ttu-id="6be62-120">**Миррорикон** не экспортируется по имени или объявлено в общедоступном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="6be62-120">**MirrorIcon** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="6be62-121">Чтобы использовать его, необходимо использовать [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и запросить порядковый номер 414 из ComCtl32.dll для получения указателя на функцию.</span><span class="sxs-lookup"><span data-stu-id="6be62-121">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 414 from ComCtl32.dll to obtain a function pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6be62-122">Требования</span><span class="sxs-lookup"><span data-stu-id="6be62-122">Requirements</span></span>



| <span data-ttu-id="6be62-123">Требование</span><span class="sxs-lookup"><span data-stu-id="6be62-123">Requirement</span></span> | <span data-ttu-id="6be62-124">Значение</span><span class="sxs-lookup"><span data-stu-id="6be62-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6be62-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6be62-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6be62-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6be62-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="6be62-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6be62-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6be62-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6be62-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="6be62-129">DLL</span><span class="sxs-lookup"><span data-stu-id="6be62-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6be62-130"><dt>Comctl32.dll (версия 5,81 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="6be62-130"><dt>Comctl32.dll (version 5.81 or later)</dt></span></span> </dl> |



 

