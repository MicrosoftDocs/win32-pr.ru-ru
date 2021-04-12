---
description: Содержит сведения о функции Криптуидлгвиевсигнеринфо.
ms.assetid: 2b76de4f-4b35-477e-a67e-435434e066c6
title: Структура CRYPTUI_VIEWSIGNERINFO_STRUCT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_VIEWSIGNERINFO_STRUCT
- CRYPTUI_VIEWSIGNERINFO_STRUCTA
- CRYPTUI_VIEWSIGNERINFO_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: da150da6b5115e20a78a4edca64a5c9a97f66132
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080780"
---
# <a name="cryptui_viewsignerinfo_struct-structure"></a><span data-ttu-id="d4d30-103">\_ \_ Структура структуры динамической компоновки Cryptui виевсигнеринфо</span><span class="sxs-lookup"><span data-stu-id="d4d30-103">CRYPTUI\_VIEWSIGNERINFO\_STRUCT structure</span></span>

<span data-ttu-id="d4d30-104">\[Структура **\_ \_ структуры динамической компоновки Cryptui виевсигнеринфо** доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="d4d30-104">\[The **CRYPTUI\_VIEWSIGNERINFO\_STRUCT** structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d4d30-105">В последующих версиях он может быть изменен или недоступен.\]</span><span class="sxs-lookup"><span data-stu-id="d4d30-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="d4d30-106">Структура **\_ \_ структуры динамической компоновки Cryptui виевсигнеринфо** содержит сведения о функции [**криптуидлгвиевсигнеринфо**](cryptuidlgviewsignerinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="d4d30-106">The **CRYPTUI\_VIEWSIGNERINFO\_STRUCT** structure contains information for the [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="d4d30-107">Эта структура не объявлена в опубликованном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="d4d30-107">This structure is not declared in a published header file.</span></span> <span data-ttu-id="d4d30-108">Чтобы использовать эту структуру, объявите ее в точно указанном формате.</span><span class="sxs-lookup"><span data-stu-id="d4d30-108">To use this structure, declare it in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d4d30-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4d30-109">Syntax</span></span>


```C++
typedef struct tagCRYPTUI_VIEWSIGNERINFO_STRUCT {
  DWORD            dwSize;
  HWND             hwndParent;
  DWORD            dwFlags;
  LPCTSTR          szTitle;
  CMSG_SIGNER_INFO *pSignerInfo;
  HCRYPTMSG        hMsg;
  LPCSTR           pszOID;
  DWORD_PTR        dwReserved;
  DWORD            cStores;
  HCERTSTORE       *rghStores;
  DWORD            cPropSheetPages;
  LPCPROPSHEETPAGE rgPropSheetPages;
} CRYPTUI_VIEWSIGNERINFO_STRUCT, *PCRYPTUI_VIEWSIGNERINFO_STRUCT;
```



## <a name="members"></a><span data-ttu-id="d4d30-110">Члены</span><span class="sxs-lookup"><span data-stu-id="d4d30-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="d4d30-111">**двсизе**</span><span class="sxs-lookup"><span data-stu-id="d4d30-111">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="d4d30-112">Размер данной структуры (в байтах).</span><span class="sxs-lookup"><span data-stu-id="d4d30-112">The size, in bytes, of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="d4d30-113">**хвндпарент**</span><span class="sxs-lookup"><span data-stu-id="d4d30-113">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="d4d30-114">Маркер окна, который будет родительским по отношению к диалоговому окну.</span><span class="sxs-lookup"><span data-stu-id="d4d30-114">The handle of the window to be the parent of the dialog box.</span></span> <span data-ttu-id="d4d30-115">Этот элемент может иметь **значение NULL** , если диалоговое окно не должно иметь родителя.</span><span class="sxs-lookup"><span data-stu-id="d4d30-115">This member can be **NULL** if the dialog box should have no parent.</span></span>

</dd> <dt>

<span data-ttu-id="d4d30-116">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="d4d30-116">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d4d30-117">Набор флагов, изменяющий поведение функции [**криптуидлгвиевсигнеринфо**](cryptuidlgviewsignerinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="d4d30-117">A set of flags that modifies the behavior of the [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) function.</span></span> <span data-ttu-id="d4d30-118">В настоящее время флаги не определены, поэтому этот элемент должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="d4d30-118">There are no flags currently defined, so this member must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d4d30-119">**сзтитле**</span><span class="sxs-lookup"><span data-stu-id="d4d30-119">**szTitle**</span></span>
</dt> <dd>

<span data-ttu-id="d4d30-120">Указатель на строку, завершающуюся нулем, которая содержит заголовок, отображаемый в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="d4d30-120">A pointer to a null-terminated string that contains the title to be displayed in the dialog box.</span></span> <span data-ttu-id="d4d30-121">Если этот член имеет **значение NULL**, используется заголовок по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d4d30-121">If this member is **NULL**, a default title is used.</span></span>

</dd> <dt>

<span data-ttu-id="d4d30-122">**псигнеринфо**</span><span class="sxs-lookup"><span data-stu-id="d4d30-122">**pSignerInfo**</span></span>
</dt> <dd>

<span data-ttu-id="d4d30-123">Указатель на [**\_ \_ информационную структуру КМСГ Sign**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) , которая содержит сведения о подписавшем для вывода.</span><span class="sxs-lookup"><span data-stu-id="d4d30-123">A pointer to a [**CMSG\_SIGNER\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) structure that contains the signer information to display.</span></span>

</dd> <dt>

<span data-ttu-id="d4d30-124">**хмсг**</span><span class="sxs-lookup"><span data-stu-id="d4d30-124">**hMsg**</span></span>
</dt> <dd>

<span data-ttu-id="d4d30-125">Маркер сообщения, из которого были извлечены сведения о подписавшем.</span><span class="sxs-lookup"><span data-stu-id="d4d30-125">The handle of the message that the signer information was extracted from.</span></span>

</dd> <dt>

<span data-ttu-id="d4d30-126">**псзоид**</span><span class="sxs-lookup"><span data-stu-id="d4d30-126">**pszOID**</span></span>
</dt> <dd>

<span data-ttu-id="d4d30-127">Указатель на строку ANSI, заканчивающуюся нулем, которая содержит строковое представление [*идентификатора объекта*](../secgloss/o-gly.md) (OID), обозначающее, для какого сертификата должен быть проверен сертификат.</span><span class="sxs-lookup"><span data-stu-id="d4d30-127">A pointer to a null-terminated ANSI string that contains the string representation of the [*object identifier*](../secgloss/o-gly.md) (OID) that signifies what the certificate that did the signing should be validated for.</span></span> <span data-ttu-id="d4d30-128">Например, если этот метод вызывается для просмотра подписи [*списка доверия сертификатов*](../secgloss/c-gly.md) (CTL), необходимо передать строку OID для **\_ \_ \_ \_ подписи использования сзоид ключевого отношения доверия** .</span><span class="sxs-lookup"><span data-stu-id="d4d30-128">For example, if this is being called to view the signature of a [*certificate trust list*](../secgloss/c-gly.md) (CTL), the **szOID\_KP\_CTL\_USAGE\_SIGNING** OID string should be passed in.</span></span> <span data-ttu-id="d4d30-129">Если этот член имеет **значение NULL**, сертификат не проверяется на наличие сведений об использовании.</span><span class="sxs-lookup"><span data-stu-id="d4d30-129">If this member is **NULL**, the certificate is not validated for usages.</span></span>

</dd> <dt>

<span data-ttu-id="d4d30-130">**двресервед**</span><span class="sxs-lookup"><span data-stu-id="d4d30-130">**dwReserved**</span></span>
</dt> <dd>

<span data-ttu-id="d4d30-131">Этот параметр в настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="d4d30-131">This parameter is not currently used.</span></span> <span data-ttu-id="d4d30-132">Этот элемент должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d4d30-132">This member must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d4d30-133">**ксторес**</span><span class="sxs-lookup"><span data-stu-id="d4d30-133">**cStores**</span></span>
</dt> <dd>

<span data-ttu-id="d4d30-134">Число элементов в массиве **ргхсторес** .</span><span class="sxs-lookup"><span data-stu-id="d4d30-134">The number of elements in the **rghStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="d4d30-135">**ргхсторес**</span><span class="sxs-lookup"><span data-stu-id="d4d30-135">**rghStores**</span></span>
</dt> <dd>

<span data-ttu-id="d4d30-136">Массив значений **хцертсторе** , представляющих другие хранилища сертификатов для поиска сертификата, подписавшего сообщение.</span><span class="sxs-lookup"><span data-stu-id="d4d30-136">An array of **HCERTSTORE** values that represent the other certificate stores to search for the certificate that signed the message.</span></span> <span data-ttu-id="d4d30-137">Если этот член имеет **значение NULL**, дополнительные хранилища не ищутся.</span><span class="sxs-lookup"><span data-stu-id="d4d30-137">If this member is **NULL**, no additional stores are searched.</span></span> <span data-ttu-id="d4d30-138">Элемент **ксторес** содержит количество элементов в этом массиве.</span><span class="sxs-lookup"><span data-stu-id="d4d30-138">The **cStores** member contains the number of elements in this array.</span></span>

</dd> <dt>

<span data-ttu-id="d4d30-139">**кпропшитпажес**</span><span class="sxs-lookup"><span data-stu-id="d4d30-139">**cPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="d4d30-140">Число элементов в массиве **ргпропшитпажес** .</span><span class="sxs-lookup"><span data-stu-id="d4d30-140">The number of elements in the **rgPropSheetPages** array.</span></span>

</dd> <dt>

<span data-ttu-id="d4d30-141">**ргпропшитпажес**</span><span class="sxs-lookup"><span data-stu-id="d4d30-141">**rgPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="d4d30-142">Массив указателей структуры [**пропшитпаже**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) , которые определяют все дополнительные страницы, отображаемые в стандартном диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="d4d30-142">An array of [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) structure pointers that define any extra pages to display in the standard dialog box.</span></span> <span data-ttu-id="d4d30-143">Если этот член имеет **значение NULL**, дополнительные страницы отображаться не будут.</span><span class="sxs-lookup"><span data-stu-id="d4d30-143">If this member is **NULL**, no additional pages will be displayed.</span></span> <span data-ttu-id="d4d30-144">Элемент **кпропшитпажес** содержит количество элементов в этом массиве.</span><span class="sxs-lookup"><span data-stu-id="d4d30-144">The **cPropSheetPages** member contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4d30-145">Требования</span><span class="sxs-lookup"><span data-stu-id="d4d30-145">Requirements</span></span>



| <span data-ttu-id="d4d30-146">Требование</span><span class="sxs-lookup"><span data-stu-id="d4d30-146">Requirement</span></span> | <span data-ttu-id="d4d30-147">Значение</span><span class="sxs-lookup"><span data-stu-id="d4d30-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d30-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4d30-148">Minimum supported client</span></span><br/> | <span data-ttu-id="d4d30-149">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d4d30-149">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="d4d30-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4d30-150">Minimum supported server</span></span><br/> | <span data-ttu-id="d4d30-151">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d4d30-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d4d30-152">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="d4d30-152">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d4d30-153">**Динамической компоновки Cryptui \_ ВИЕВСИГНЕРИНФО \_ структв** (Юникод) и **динамической компоновки Cryptui \_ виевсигнеринфо \_ struct** a (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d4d30-153">**CRYPTUI\_VIEWSIGNERINFO\_STRUCTW** (Unicode) and **CRYPTUI\_VIEWSIGNERINFO\_STRUCTA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d4d30-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4d30-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d30-155">**криптуидлгвиевсигнеринфо**</span><span class="sxs-lookup"><span data-stu-id="d4d30-155">**CryptUIDlgViewSignerInfo**</span></span>](cryptuidlgviewsignerinfo.md)
</dt> </dl>

 

 
