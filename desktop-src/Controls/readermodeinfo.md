---
title: Структура РЕАДЕРМОДЕИНФО
description: Содержит сведения, необходимые для инициализации функции Дореадермоде.
ms.assetid: 7b9c73bc-b093-4592-befd-67508fb86fe0
keywords:
- Элементы управления Windows структуры РЕАДЕРМОДЕИНФО
- Указатель структуры ПРЕАДЕРМОДЕИНФО элементы управления Windows
topic_type:
- apiref
api_name:
- READERMODEINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2dacf0fc59ef62447ca12b7a470689e13967d687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491745"
---
# <a name="readermodeinfo-structure"></a><span data-ttu-id="6942e-105">Структура РЕАДЕРМОДЕИНФО</span><span class="sxs-lookup"><span data-stu-id="6942e-105">READERMODEINFO structure</span></span>

<span data-ttu-id="6942e-106">\[**Реадермодеинфо** поддерживается в Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="6942e-106">\[**READERMODEINFO** is supported through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="6942e-107">В последующих версиях он может не поддерживаться.\]</span><span class="sxs-lookup"><span data-stu-id="6942e-107">It might be unsupported in subsequent versions.\]</span></span>

<span data-ttu-id="6942e-108">Содержит сведения, необходимые для инициализации функции [**дореадермоде**](doreadermode.md) .</span><span class="sxs-lookup"><span data-stu-id="6942e-108">Contains information required to initialize the [**DoReaderMode**](doreadermode.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="6942e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6942e-109">Syntax</span></span>


```C++
typedef struct tagReaderModeInfo {
  UINT                       cbSize;
  HWND                       hwnd;
  DWORD                      fFlags;
  LPRECT                     prc;
  PFNREADERSCROLL            pfnScroll;
  PFNREADERTRANSLATEDISPATCH fFlags;
  LPARAM                     lParam;
} READERMODEINFO, *PREADERMODEINFO;
```



## <a name="members"></a><span data-ttu-id="6942e-110">Члены</span><span class="sxs-lookup"><span data-stu-id="6942e-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="6942e-111">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="6942e-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="6942e-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6942e-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6942e-113">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6942e-113">Required.</span></span> <span data-ttu-id="6942e-114">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="6942e-114">The size of the structure, in bytes.</span></span> <span data-ttu-id="6942e-115">Перед вызовом [**дореадермоде**](doreadermode.md)задайте для этого параметра значение **sizeof (реадермоде)** .</span><span class="sxs-lookup"><span data-stu-id="6942e-115">Set this parameter to **sizeof(READERMODE)** before you call [**DoReaderMode**](doreadermode.md).</span></span>

</dd> <dt>

<span data-ttu-id="6942e-116">**HWND**</span><span class="sxs-lookup"><span data-stu-id="6942e-116">**hwnd**</span></span>
</dt> <dd>

<span data-ttu-id="6942e-117">Тип: **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6942e-117">Type: **[**HWND**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6942e-118">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6942e-118">Required.</span></span> <span data-ttu-id="6942e-119">Маркер окна, используемый для режима чтения.</span><span class="sxs-lookup"><span data-stu-id="6942e-119">The handle of the window to be used for reader mode.</span></span>

</dd> <dt>

<span data-ttu-id="6942e-120">**ффлагс**</span><span class="sxs-lookup"><span data-stu-id="6942e-120">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="6942e-121">Тип: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6942e-121">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6942e-122">Флаги. Настройка функциональных возможностей окна режима модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="6942e-122">Flags customizing the functionality of the reader mode window.</span></span> <span data-ttu-id="6942e-123">Этот параметр может иметь значение 0; в противном случае одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6942e-123">This parameter can be 0; otherwise, one or more of the following values.</span></span>



| <span data-ttu-id="6942e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="6942e-124">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="6942e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="6942e-125">Meaning</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RMF_ZEROCURSOR"></span><span id="rmf_zerocursor"></span><dl> <span data-ttu-id="6942e-126"><dt>**РМФ \_ ЗЕРОКУРСОР**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="6942e-126"><dt>**RMF\_ZEROCURSOR**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="6942e-127">Задает курсор в центре области, заданной в **PRC**.</span><span class="sxs-lookup"><span data-stu-id="6942e-127">Sets the cursor in the center of the area specified in **prc**.</span></span> <span data-ttu-id="6942e-128">Если этот флаг не указан, позиции курсора остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="6942e-128">If this flag is not specified, the cursor position remains unchanged.</span></span><br/> |
| <span id="RMF_VERTICALONLY"></span><span id="rmf_verticalonly"></span><dl> <span data-ttu-id="6942e-129"><dt>**РМФ \_ ВЕРТИКАЛОНЛИ**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="6942e-129"><dt>**RMF\_VERTICALONLY**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="6942e-130">Разрешает только вертикальную прокрутку.</span><span class="sxs-lookup"><span data-stu-id="6942e-130">Allows only vertical scrolling.</span></span><br/>                                                                                                       |
| <span id="RMF_HORIZONTALONLY"></span><span id="rmf_horizontalonly"></span><dl> <span data-ttu-id="6942e-131"><dt>**РМФ \_ ХОРИЗОНТАЛОНЛИ**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="6942e-131"><dt>**RMF\_HORIZONTALONLY**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="6942e-132">Разрешает только горизонтальную прокрутку.</span><span class="sxs-lookup"><span data-stu-id="6942e-132">Allows only horizontal scrolling.</span></span><br/>                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="6942e-133">**PRC**</span><span class="sxs-lookup"><span data-stu-id="6942e-133">**prc**</span></span>
</dt> <dd>

<span data-ttu-id="6942e-134">Тип: **лпрект**</span><span class="sxs-lookup"><span data-stu-id="6942e-134">Type: **LPRECT**</span></span>

</dd> <dd>

<span data-ttu-id="6942e-135">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , указывающую область прокрутки в окне режима чтения.</span><span class="sxs-lookup"><span data-stu-id="6942e-135">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the scrolling area in the reader mode window.</span></span> <span data-ttu-id="6942e-136">Если этот элемент имеет **значение NULL**, то в качестве области прокрутки используется все окно.</span><span class="sxs-lookup"><span data-stu-id="6942e-136">If this member is **NULL**, then the entire window is used as the scrolling area.</span></span>

</dd> <dt>

<span data-ttu-id="6942e-137">**пфнскролл**</span><span class="sxs-lookup"><span data-stu-id="6942e-137">**pfnScroll**</span></span>
</dt> <dd>

<span data-ttu-id="6942e-138">Тип: **пфнреадерскролл**</span><span class="sxs-lookup"><span data-stu-id="6942e-138">Type: **PFNREADERSCROLL**</span></span>

</dd> <dd>

<span data-ttu-id="6942e-139">Указатель на определяемую приложением функцию обратного вызова [*реадерскролл*](readerscroll.md) , используемую для уведомления приложения о том, что окно необходимо прокрутить в определенном направлении.</span><span class="sxs-lookup"><span data-stu-id="6942e-139">A pointer to an application-defined [*ReaderScroll*](readerscroll.md) callback function used to notify the application that the window needs to be scrolled in a particular direction.</span></span>

</dd> <dt>

<span data-ttu-id="6942e-140">**ффлагс**</span><span class="sxs-lookup"><span data-stu-id="6942e-140">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="6942e-141">Тип: **пфнреадертранслатедиспатч**</span><span class="sxs-lookup"><span data-stu-id="6942e-141">Type: **PFNREADERTRANSLATEDISPATCH**</span></span>

</dd> <dd>

<span data-ttu-id="6942e-142">Указатель на определяемую приложением функцию обратного вызова [*транслатедиспатч*](translatedispatch.md) , используемую для получения первого уведомления о любых сообщениях, отправленных в окно режима модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="6942e-142">A pointer to an application-defined [*TranslateDispatch*](translatedispatch.md) callback function used to get first notification of any messages sent to the reader mode window.</span></span>

</dd> <dt>

<span data-ttu-id="6942e-143">**lParam**</span><span class="sxs-lookup"><span data-stu-id="6942e-143">**lParam**</span></span>
</dt> <dd>

<span data-ttu-id="6942e-144">Тип: **[ **lParam** .](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6942e-144">Type: **[**LPARAM**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="6942e-145">Дополнительные сведения, необходимые для приложения, считываются вызывающим объектом в функции обратного вызова [*реадерскролл*](readerscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="6942e-145">Additional information as needed by the application, read by the caller in the [*ReaderScroll*](readerscroll.md) callback function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6942e-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6942e-146">Remarks</span></span>

<span data-ttu-id="6942e-147">Эта структура не объявлена ни в одном общедоступном заголовке.</span><span class="sxs-lookup"><span data-stu-id="6942e-147">This structure is not declared in any public header.</span></span> <span data-ttu-id="6942e-148">Чтобы использовать его, необходимо включить объявление, показанное выше, в свой собственный заголовок.</span><span class="sxs-lookup"><span data-stu-id="6942e-148">To use it, you must include the declaration shown above in your own header.</span></span>

## <a name="requirements"></a><span data-ttu-id="6942e-149">Требования</span><span class="sxs-lookup"><span data-stu-id="6942e-149">Requirements</span></span>



| <span data-ttu-id="6942e-150">Требование</span><span class="sxs-lookup"><span data-stu-id="6942e-150">Requirement</span></span> | <span data-ttu-id="6942e-151">Значение</span><span class="sxs-lookup"><span data-stu-id="6942e-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="6942e-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6942e-152">Minimum supported client</span></span><br/> | <span data-ttu-id="6942e-153">Windows Vista, \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6942e-153">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6942e-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6942e-154">Minimum supported server</span></span><br/> | <span data-ttu-id="6942e-155">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6942e-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

