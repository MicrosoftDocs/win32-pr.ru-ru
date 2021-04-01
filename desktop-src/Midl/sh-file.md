---
title: Ключевое слово sh_file
description: '\_Ключевое слово \ SH File \ указывает, что системный объект является обработчиком файла.'
keywords:
- sh_file ключевого слова MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: f7d2ae0ef4a8166f90700267fa8459525ad4be2f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "104350965"
---
# <a name="sh_file-keyword"></a><span data-ttu-id="05c66-104">SH \_ File, ключевое слово</span><span class="sxs-lookup"><span data-stu-id="05c66-104">sh\_file keyword</span></span>

<span data-ttu-id="05c66-105">Ключевое слово **sh \_ File** указывает, что объект `system_handle` содержит маркер файла.</span><span class="sxs-lookup"><span data-stu-id="05c66-105">The **sh\_file** keyword specifies that a `system_handle` holds a handle to a file.</span></span>

``` syntax
[system_handle(sh_file)]

[system_handle(sh_file, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="05c66-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="05c66-106">Parameters</span></span>

<span data-ttu-id="05c66-107">Это ключевое слово является параметром для [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="05c66-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="05c66-108">В документации по [**system_handle**](system-handle.md) также содержатся сведения о необязательном использовании параметра *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="05c66-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="05c66-109">Поведение по умолчанию `DUPLICATE_SAME_ACCESS` для каждой спецификации [ **функции дупликатехандле**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="05c66-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="05c66-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05c66-110">Remarks</span></span>

<span data-ttu-id="05c66-111">Чтобы использовать это ключевое слово с `system_handle` атрибутом, `-target` необходимо установить для флага значение `NT100` (или более высокий) при выполнении midl.exe.</span><span class="sxs-lookup"><span data-stu-id="05c66-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="05c66-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="05c66-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT WriteThisFile([in, system_handle(sh_file)] HANDLE file);

    HRESULT GetFileToRead([out, system_handle(sh_file, READ_CONTROL | SYNCHRONIZE | FILE_READ_DATA | FILE_READ_keywordS | FILE_READ_EA)] HANDLE* pReadThisFile);
}
```

## <a name="requirements"></a><span data-ttu-id="05c66-113">Требования</span><span class="sxs-lookup"><span data-stu-id="05c66-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="05c66-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="05c66-114">Minimum supported client</span></span> | <span data-ttu-id="05c66-115">Юбилейное обновление Windows 10 (версия 1607, сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="05c66-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="05c66-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="05c66-116">Minimum supported server</span></span> | <span data-ttu-id="05c66-117">Windows Server 2016 (сборка 14393)</span><span class="sxs-lookup"><span data-stu-id="05c66-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="05c66-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05c66-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05c66-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="05c66-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="05c66-120">Безопасность файлов и права доступа</span><span class="sxs-lookup"><span data-stu-id="05c66-120">File Security and Access Rights</span></span>](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="05c66-121">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="05c66-121">DirectComposition</span></span>](/windows/win32/api/_directcomp/)
</dt> <dt>

[<span data-ttu-id="05c66-122">Функция **дкомпоситионкреатесурфацехандле**</span><span class="sxs-lookup"><span data-stu-id="05c66-122">**DCompositionCreateSurfaceHandle** function</span></span>](/windows/win32/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle)
</dt> <dt>
