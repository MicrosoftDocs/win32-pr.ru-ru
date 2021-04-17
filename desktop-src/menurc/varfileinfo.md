---
title: Структура Варфилеинфо
description: Представляет организацию данных в ресурсе версии файла. Он содержит сведения о версии, не зависящие от конкретного языка и сочетания кодовой страницы.
ms.assetid: 3b667778-fb08-4195-a88e-ac04baf45fee
keywords:
- Меню структуры Варфилеинфо и другие ресурсы
topic_type:
- apiref
api_name:
- VarFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26326403abef41d131bf25acf5d5d8be7728cd0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710515"
---
# <a name="varfileinfo-structure"></a><span data-ttu-id="c702a-105">Структура Варфилеинфо</span><span class="sxs-lookup"><span data-stu-id="c702a-105">VarFileInfo structure</span></span>

<span data-ttu-id="c702a-106">Представляет организацию данных в ресурсе версии файла.</span><span class="sxs-lookup"><span data-stu-id="c702a-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="c702a-107">Он содержит сведения о версии, не зависящие от конкретного языка и сочетания кодовой страницы.</span><span class="sxs-lookup"><span data-stu-id="c702a-107">It contains version information not dependent on a particular language and code page combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="c702a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c702a-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  Var   Children;
} VarFileInfo;
```



## <a name="members"></a><span data-ttu-id="c702a-109">Члены</span><span class="sxs-lookup"><span data-stu-id="c702a-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="c702a-110">**вленгс**</span><span class="sxs-lookup"><span data-stu-id="c702a-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="c702a-111">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="c702a-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c702a-112">Длина всего блока **варфилеинфо** в байтах, включая все структуры, указанные **дочерним** элементом.</span><span class="sxs-lookup"><span data-stu-id="c702a-112">The length, in bytes, of the entire **VarFileInfo** block, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="c702a-113">**ввалуеленгс**</span><span class="sxs-lookup"><span data-stu-id="c702a-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="c702a-114">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="c702a-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c702a-115">Этот элемент всегда равен нулю.</span><span class="sxs-lookup"><span data-stu-id="c702a-115">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="c702a-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="c702a-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="c702a-117">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="c702a-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c702a-118">Тип данных в ресурсе версии.</span><span class="sxs-lookup"><span data-stu-id="c702a-118">The type of data in the version resource.</span></span> <span data-ttu-id="c702a-119">Этот элемент равен 1, если ресурс версии содержит текстовые данные, и 0, если ресурс версии содержит двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="c702a-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="c702a-120">**сзкэй**</span><span class="sxs-lookup"><span data-stu-id="c702a-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="c702a-121">Тип: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="c702a-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="c702a-122">Строка Юникода L "Варфилеинфо".</span><span class="sxs-lookup"><span data-stu-id="c702a-122">The Unicode string L"VarFileInfo".</span></span>

</dd> <dt>

<span data-ttu-id="c702a-123">**Заполнение**</span><span class="sxs-lookup"><span data-stu-id="c702a-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="c702a-124">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="c702a-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c702a-125">Столько нуля слов, сколько необходимо для выровняйте **дочернего** элемента на 32-разрядной границе.</span><span class="sxs-lookup"><span data-stu-id="c702a-125">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="c702a-126">**Children**</span><span class="sxs-lookup"><span data-stu-id="c702a-126">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="c702a-127">Тип: **[ **var**](var-str.md)**</span><span class="sxs-lookup"><span data-stu-id="c702a-127">Type: **[**Var**](var-str.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c702a-128">Обычно содержит список языков, поддерживаемых приложением или библиотекой DLL.</span><span class="sxs-lookup"><span data-stu-id="c702a-128">Typically contains a list of languages that the application or DLL supports.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c702a-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c702a-129">Remarks</span></span>

<span data-ttu-id="c702a-130">Эта структура не является истинной структурой языка C, так как она содержит члены переменной длины.</span><span class="sxs-lookup"><span data-stu-id="c702a-130">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="c702a-131">Эта структура была создана только для описания организации данных в ресурсе версии и не отображается ни в одном из файлов заголовков, поставляемых вместе с пакетом средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="c702a-131">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="c702a-132">**Дочерние** элементы структуры [**VS \_ versionInfo**](vs-versioninfo.md) могут содержать ноль или одну структуру **варфилеинфо** .</span><span class="sxs-lookup"><span data-stu-id="c702a-132">The **Children** member of the [**VS\_VERSIONINFO**](vs-versioninfo.md) structure may contain zero or one **VarFileInfo** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="c702a-133">Требования</span><span class="sxs-lookup"><span data-stu-id="c702a-133">Requirements</span></span>



| <span data-ttu-id="c702a-134">Требование</span><span class="sxs-lookup"><span data-stu-id="c702a-134">Requirement</span></span> | <span data-ttu-id="c702a-135">Значение</span><span class="sxs-lookup"><span data-stu-id="c702a-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c702a-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c702a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c702a-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c702a-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c702a-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c702a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c702a-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c702a-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c702a-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c702a-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="c702a-141">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="c702a-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c702a-142">**Var**</span><span class="sxs-lookup"><span data-stu-id="c702a-142">**Var**</span></span>](var-str.md)
</dt> <dt>

[<span data-ttu-id="c702a-143">**VS \_ versionInfo**</span><span class="sxs-lookup"><span data-stu-id="c702a-143">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="c702a-144">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="c702a-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c702a-145">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="c702a-145">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





