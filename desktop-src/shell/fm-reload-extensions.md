---
description: Отправляется расширением диспетчера файлов (или другим приложением), чтобы диспетчер файлов перезагружал все библиотеки DLL расширения, перечисленные в \[ разделе "надстройки" \] файла Winfile.ini.
ms.assetid: 5103a986-5f45-4deb-aaae-c6e87cb60051
title: Сообщение FM_RELOAD_EXTENSIONS (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_RELOAD_EXTENSIONS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: 9e82ec9ec638cb70cc7b571ed9e5e76d604cd4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985517"
---
# <a name="fm_reload_extensions-message"></a><span data-ttu-id="50793-103">\_Сообщение о перезагрузке \_ расширений FM</span><span class="sxs-lookup"><span data-stu-id="50793-103">FM\_RELOAD\_EXTENSIONS message</span></span>

<span data-ttu-id="50793-104">Отправляется расширением диспетчера файлов (или другим приложением), чтобы диспетчер файлов перезагружал все библиотеки DLL расширения, перечисленные в \[ разделе "надстройки" \] файла Winfile.ini.</span><span class="sxs-lookup"><span data-stu-id="50793-104">Sent by a File Manager extension (or another application) to cause File Manager to reload all extension DLLs listed in the \[AddOns\] section of the Winfile.ini file.</span></span>

## <a name="parameters"></a><span data-ttu-id="50793-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="50793-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50793-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50793-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50793-107">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="50793-107">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="50793-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50793-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50793-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="50793-109">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50793-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50793-110">Return value</span></span>

<span data-ttu-id="50793-111">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="50793-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50793-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="50793-112">Remarks</span></span>

<span data-ttu-id="50793-113">Другие приложения могут использовать функцию посылки [**сообщений**](/windows/win32/api/winuser/nf-winuser-postmessagea) для отправки этого сообщения в Диспетчер файлов.</span><span class="sxs-lookup"><span data-stu-id="50793-113">Other applications can use the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function to send this message to File Manager.</span></span> <span data-ttu-id="50793-114">Чтобы получить соответствующий обработчик окна диспетчера файлов, приложение может указать "ВФС \_ Frame" в качестве параметра *лпсзкласснаме* в вызове функции [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) .</span><span class="sxs-lookup"><span data-stu-id="50793-114">To obtain the appropriate File Manager window handle, an application can specify "WFS\_Frame" as the *lpszClassName* parameter in a call to the [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="50793-115">Требования</span><span class="sxs-lookup"><span data-stu-id="50793-115">Requirements</span></span>



| <span data-ttu-id="50793-116">Требование</span><span class="sxs-lookup"><span data-stu-id="50793-116">Requirement</span></span> | <span data-ttu-id="50793-117">Значение</span><span class="sxs-lookup"><span data-stu-id="50793-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="50793-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50793-118">Minimum supported client</span></span><br/> | <span data-ttu-id="50793-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50793-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="50793-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50793-120">Minimum supported server</span></span><br/> | <span data-ttu-id="50793-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50793-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="50793-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="50793-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="50793-123"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="50793-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50793-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50793-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50793-125">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="50793-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 
