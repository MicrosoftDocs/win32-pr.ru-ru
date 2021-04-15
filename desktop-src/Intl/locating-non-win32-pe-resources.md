---
description: Поиск ресурсов, отличных от Win32 PE
ms.assetid: 12f0b78e-ca85-443a-94ea-6bec5aa40c06
title: Поиск ресурсов, отличных от Win32 PE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 079288cd6200eb64289f474636cbc8dc046c1e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683001"
---
# <a name="locating-non-win32-pe-resources"></a><span data-ttu-id="60706-103">Поиск ресурсов, отличных от Win32 PE</span><span class="sxs-lookup"><span data-stu-id="60706-103">Locating Non-Win32 PE Resources</span></span>

<span data-ttu-id="60706-104">Для размещения ресурсов, отличных от Win32 PE, приложение должно сначала вызвать функцию [**жетфилемуипас**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) для размещения файла ресурсов, зависящего от языка, из которого загружаются ресурсы.</span><span class="sxs-lookup"><span data-stu-id="60706-104">To locate non-Win32 PE resources, your application should first call the [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) function to locate the language-specific resource file from which to load resources.</span></span> <span data-ttu-id="60706-105">Если приложение имеет следующие системные параметры языка, оно должно вызывать функцию с \_ именем языка MUI \_ \| \_ \_ предпочтительные \_ языки интерфейса пользователя MUI \_ , указанные для *DwFlags* , и **значение NULL** , указанное для *пвсзлангуаже*.</span><span class="sxs-lookup"><span data-stu-id="60706-105">If the application is following system language settings, it must call the function with MUI\_LANGUAGE\_NAME \| MUI\_USER\_PREFERRED\_UI\_LANGUAGES specified for *dwFlags* and **NULL** specified for *pwszLanguage*.</span></span> <span data-ttu-id="60706-106">Если приложение имеет следующие параметры языка приложения, оно использует **жетфилемуипас** , чтобы определить, существует ли зависящий от языка файл, указав язык в параметре *пвсзлангуаже* .</span><span class="sxs-lookup"><span data-stu-id="60706-106">If the application is following application-specific language settings, it uses **GetFileMUIPath** to determine if a language-specific file exists by specifying the language in the *pwszLanguage* parameter.</span></span>

<span data-ttu-id="60706-107">После вызова [**жетфилемуипас**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)приложение должно определить пользовательские функции, чтобы загрузить модуль ресурсов и загрузить из него определенные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="60706-107">After the call to [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath), the application must define custom functionality to load the resource module and load specific resources from it.</span></span> <span data-ttu-id="60706-108">Например, если используется файл ресурсов. txt или. XML, приложение должно использовать для загрузки файла TXT или XML Parser, а затем анализировать содержимое файла для каждого необходимого ресурса.</span><span class="sxs-lookup"><span data-stu-id="60706-108">For example, if you are using a .txt or .xml resource file, the application must use a TXT or XML parser to load the file and then parse the contents of the file for each required resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60706-109">См. также</span><span class="sxs-lookup"><span data-stu-id="60706-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60706-110">Использование многоязыкового интерфейса пользователя</span><span class="sxs-lookup"><span data-stu-id="60706-110">Using Multilingual User Interface</span></span>](using-multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="60706-111">**жетфилемуипас**</span><span class="sxs-lookup"><span data-stu-id="60706-111">**GetFileMUIPath**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)
</dt> </dl>

 

 



