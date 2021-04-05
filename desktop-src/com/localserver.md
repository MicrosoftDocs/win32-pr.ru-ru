---
title: локалсервер
description: Указывает полный путь к 16-разрядному приложению локального сервера.
ms.assetid: 6eadadd5-f4d3-4e0d-9491-2ea366861aa7
keywords:
- COM раздела реестра Локалсервер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7413f9d7c4d17e9498e80d19b70192fbb21911b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068318"
---
# <a name="localserver"></a><span data-ttu-id="d2bcc-104">локалсервер</span><span class="sxs-lookup"><span data-stu-id="d2bcc-104">LocalServer</span></span>

<span data-ttu-id="d2bcc-105">Указывает полный путь к 16-разрядному приложению локального сервера.</span><span class="sxs-lookup"><span data-stu-id="d2bcc-105">Specifies the full path to a 16-bit local server application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="d2bcc-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="d2bcc-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer = path
```

## <a name="remarks"></a><span data-ttu-id="d2bcc-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2bcc-107">Remarks</span></span>

<span data-ttu-id="d2bcc-108">Это значение **reg \_ SZ** , которое указывает полный путь и может содержать любые аргументы командной строки.</span><span class="sxs-lookup"><span data-stu-id="d2bcc-108">This is a **REG\_SZ** value that specifies the full path and can include any command-line arguments.</span></span>

<span data-ttu-id="d2bcc-109">COM добавляет к строке флаг "-Встраивание", поэтому приложение, использующее флаги, должно проанализировать всю строку и проверить флаг-встраивание.</span><span class="sxs-lookup"><span data-stu-id="d2bcc-109">COM appends the "-Embedding" flag to the string, so the application that uses flags must parse the whole string and check for the -Embedding flag.</span></span>

<span data-ttu-id="d2bcc-110">Чтобы запустить сервер COM Object Server в отдельной области памяти, измените значение **локалсервер** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d2bcc-110">To run a COM object server in a separate memory space, change the value of **LocalServer** as follows:</span></span>

<span data-ttu-id="d2bcc-111">**cmd/c Start/сепарате** *путь \* \* *. exe**</span><span class="sxs-lookup"><span data-stu-id="d2bcc-111">**cmd /c start /separate** *path\*\*\*.exe*\*</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2bcc-112">См. также</span><span class="sxs-lookup"><span data-stu-id="d2bcc-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2bcc-113">**LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="d2bcc-113">**LocalServer32**</span></span>](localserver32.md)
</dt> </dl>

 

 




