---
UID: ''
title: Функция Шжетфолдерпасекс
description: Извлекает путь к известной папке, определяемой параметром КНОВНФОЛДЕРИД.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: SHGetFolderPath
ms.topic: reference
req.header: Shlobj.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Shell32.lib
req.dll: API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
api_name:
- SHGetFolderPathEx
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0dfc3342f3eca5622c25d2df7319cd2323f516ff
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2020
ms.locfileid: "104983948"
---
# <a name="shgetfolderpathex-function"></a><span data-ttu-id="387fa-103">Функция Шжетфолдерпасекс</span><span class="sxs-lookup"><span data-stu-id="387fa-103">SHGetFolderPathEx function</span></span>

## <a name="description"></a><span data-ttu-id="387fa-104">Описание</span><span class="sxs-lookup"><span data-stu-id="387fa-104">Description</span></span>

<span data-ttu-id="387fa-105">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="387fa-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span>
<span data-ttu-id="387fa-106">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="387fa-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="387fa-107">Получает полный путь к известной папке, идентифицируемой [кновнфолдерид](/windows/desktop/shell/knownfolderid)папки.</span><span class="sxs-lookup"><span data-stu-id="387fa-107">Retrieves the full path of a known folder identified by the folder's [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid).</span></span>
<span data-ttu-id="387fa-108">Это расширяет [шжеткновнфолдерпас](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) , позволяя задавать начальный размер строкового буфера.</span><span class="sxs-lookup"><span data-stu-id="387fa-108">This extends [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) by allowing you to set the initial size of the string buffer.</span></span>

```cpp
HRESULT WINAPI SHGetFolderPathEx(
  _In_     REFKNOWNFOLDERID rfid,
  _In_     DWORD            dwFlags,
  _In_opt_ HANDLE           hToken,
  _Out_    LPWSTR           pszPath,
  _In_     UINT             cchPath
);
```

## <a name="parameters"></a><span data-ttu-id="387fa-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="387fa-109">Parameters</span></span>

### <a name="rfid-in"></a><span data-ttu-id="387fa-110">RFID [in]</span><span class="sxs-lookup"><span data-stu-id="387fa-110">rfid [in]</span></span>

<span data-ttu-id="387fa-111">Ссылка на **кновнфолдерид** , определяющая папку.</span><span class="sxs-lookup"><span data-stu-id="387fa-111">A reference to the **KNOWNFOLDERID** that identifies the folder.</span></span>

### <a name="dwflags-in"></a><span data-ttu-id="387fa-112">dwFlags [in]</span><span class="sxs-lookup"><span data-stu-id="387fa-112">dwFlags [in]</span></span>

<span data-ttu-id="387fa-113">Флаги, указывающие специальные параметры извлечения.</span><span class="sxs-lookup"><span data-stu-id="387fa-113">Flags that specify special retrieval options.</span></span>
<span data-ttu-id="387fa-114">Это значение может быть равно 0; в противном случае — одно или несколько значений [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) .</span><span class="sxs-lookup"><span data-stu-id="387fa-114">This value can be 0; otherwise, one or more of the [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) values.</span></span>

### <a name="htoken-in-optional"></a><span data-ttu-id="387fa-115">Хтокен [in, необязательный]</span><span class="sxs-lookup"><span data-stu-id="387fa-115">hToken [in, optional]</span></span>

<span data-ttu-id="387fa-116">[Маркер доступа](/windows/desktop/SecAuthZ/access-tokens) , представляющий конкретного пользователя.</span><span class="sxs-lookup"><span data-stu-id="387fa-116">An [access token](/windows/desktop/SecAuthZ/access-tokens) that represents a particular user.</span></span>
<span data-ttu-id="387fa-117">Если этот параметр имеет **значение NULL**, то есть наиболее распространенный способ использования, функция запрашивает у текущего пользователя доступ к известной папке.</span><span class="sxs-lookup"><span data-stu-id="387fa-117">If this parameter is **NULL**, which is the most common usage, the function requests the known folder for the current user.</span></span>

<span data-ttu-id="387fa-118">Запросите папку конкретного пользователя, передав *хтокен* этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="387fa-118">Request a specific user's folder by passing the *hToken* of that user.</span></span>
<span data-ttu-id="387fa-119">Обычно это делается в контексте службы, обладающей достаточными привилегиями для получения маркера данного пользователя.</span><span class="sxs-lookup"><span data-stu-id="387fa-119">This is typically done in the context of a service that has sufficient privileges to retrieve the token of a given user.</span></span>
<span data-ttu-id="387fa-120">Этот маркер должен быть открыт с правами [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) и [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) .</span><span class="sxs-lookup"><span data-stu-id="387fa-120">That token must be opened with [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) and [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) rights.</span></span>
<span data-ttu-id="387fa-121">В некоторых случаях также необходимо включить [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects).</span><span class="sxs-lookup"><span data-stu-id="387fa-121">In some cases, you also need to include [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects).</span></span>
<span data-ttu-id="387fa-122">Кроме передачи *хтокен* пользователя, необходимо подключить куст реестра для конкретного пользователя.</span><span class="sxs-lookup"><span data-stu-id="387fa-122">In addition to passing the user's *hToken*, the registry hive of that specific user must be mounted.</span></span>
<span data-ttu-id="387fa-123">Дополнительные сведения о проблемах, связанных с управлением доступом, см. в статье [Контроль доступа](/windows/desktop/SecAuthZ/access-control) .</span><span class="sxs-lookup"><span data-stu-id="387fa-123">See [Access Control](/windows/desktop/SecAuthZ/access-control) for further discussion of access control issues.</span></span>

<span data-ttu-id="387fa-124">При назначении параметра *хтокен* значение-1 указывает на пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="387fa-124">Assigning the *hToken* parameter a value of -1 indicates the Default User.</span></span>
<span data-ttu-id="387fa-125">Это позволяет клиентам [шжеткновнфолдерпас](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) находить расположения папок (например, папки **рабочего стола** ) для пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="387fa-125">This allows clients of [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) to find folder locations (such as the **Desktop** folder) for the Default User.</span></span>
<span data-ttu-id="387fa-126">Профиль пользователя по умолчанию дублируется при создании новой учетной записи пользователя и включает специальные папки, такие как **документы** и **Рабочий стол**.</span><span class="sxs-lookup"><span data-stu-id="387fa-126">The Default User user profile is duplicated when any new user account is created, and includes special folders such as **Documents** and **Desktop**.</span></span>
<span data-ttu-id="387fa-127">Все элементы, добавленные в папку пользователя по умолчанию, также отображаются в любой новой учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="387fa-127">Any items added to the Default User folder also appear in any new user account.</span></span>
<span data-ttu-id="387fa-128">Обратите внимание, что для доступа к папкам пользователя по умолчанию требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="387fa-128">Note that access to the Default User folders requires administrator privileges.</span></span>

### <a name="pszpath-out"></a><span data-ttu-id="387fa-129">Псзпас [out]</span><span class="sxs-lookup"><span data-stu-id="387fa-129">pszPath [out]</span></span>

<span data-ttu-id="387fa-130">Строка в Юникоде, заканчивающаяся символом NULL.</span><span class="sxs-lookup"><span data-stu-id="387fa-130">A null-terminated, Unicode string.</span></span>
<span data-ttu-id="387fa-131">Этот буфер должен иметь размер Кчпас.</span><span class="sxs-lookup"><span data-stu-id="387fa-131">This buffer must be of size cchPath.</span></span>
<span data-ttu-id="387fa-132">Когда **шжетфолдерпасекс** возвращается успешно, этот параметр содержит путь к известной папке.</span><span class="sxs-lookup"><span data-stu-id="387fa-132">When **SHGetFolderPathEx** returns successfully, this parameter contains the path for the known folder.</span></span>

### <a name="cchpath-in"></a><span data-ttu-id="387fa-133">Кчпас [in]</span><span class="sxs-lookup"><span data-stu-id="387fa-133">cchPath [in]</span></span>

<span data-ttu-id="387fa-134">Размер буфера *ппсзпас* в символах.</span><span class="sxs-lookup"><span data-stu-id="387fa-134">The size of the *ppszPath* buffer, in characters.</span></span>

## <a name="returns"></a><span data-ttu-id="387fa-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="387fa-135">Returns</span></span>

<span data-ttu-id="387fa-136">Возвращает **S_OK** в случае успеха или значение ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="387fa-136">Returns **S_OK** if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="387fa-137">Примечания</span><span class="sxs-lookup"><span data-stu-id="387fa-137">Remarks</span></span>

<span data-ttu-id="387fa-138">Так как [шжетфолдерпас](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) является оболочкой для [шжеткновнфолдерпас](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath), эта функция (**шжетфолдерпасекс**) также служит расширением для **шжетфолдерпас**.</span><span class="sxs-lookup"><span data-stu-id="387fa-138">Since [SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) is a wrapper for [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath), this function (**SHGetFolderPathEx**) also serves as an extension to **SHGetFolderPath**.</span></span>

## <a name="see-also"></a><span data-ttu-id="387fa-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="387fa-139">See also</span></span>

[<span data-ttu-id="387fa-140">кновнфолдерид</span><span class="sxs-lookup"><span data-stu-id="387fa-140">KNOWNFOLDERID</span></span>](/windows/desktop/shell/knownfolderid)

[<span data-ttu-id="387fa-141">KNOWN_FOLDER_FLAG</span><span class="sxs-lookup"><span data-stu-id="387fa-141">KNOWN_FOLDER_FLAG</span></span>](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag)

[<span data-ttu-id="387fa-142">шжетфолдерпас</span><span class="sxs-lookup"><span data-stu-id="387fa-142">SHGetFolderPath</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)

[<span data-ttu-id="387fa-143">шжеткновнфолдеридлист</span><span class="sxs-lookup"><span data-stu-id="387fa-143">SHGetKnownFolderIDList</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist)

[<span data-ttu-id="387fa-144">шжеткновнфолдерпас</span><span class="sxs-lookup"><span data-stu-id="387fa-144">SHGetKnownFolderPath</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)
