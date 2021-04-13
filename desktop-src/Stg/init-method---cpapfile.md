---
title: Метод init — Кпапфиле
description: В следующем примере кода показано, как инициализируется Кпапфиле.
ms.assetid: 8312a6b2-6f3f-4a24-8aeb-9461f3b1a905
keywords:
- Метод init — Кпапфиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4fb5729ddcf20545254e3e461070c3e68f3421
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413438"
---
# <a name="init-method---cpapfile"></a><span data-ttu-id="147c9-104">Метод init — Кпапфиле</span><span class="sxs-lookup"><span data-stu-id="147c9-104">Init Method - CPapFile</span></span>

<span data-ttu-id="147c9-105">В следующем примере кода показано, как инициализируется **кпапфиле** .</span><span class="sxs-lookup"><span data-stu-id="147c9-105">The following code example shows how **CPapFile** is initialized.</span></span>

<span data-ttu-id="147c9-106">В этом примере используется метод  **init** **кпапфиле** из папфиле. cpp.</span><span class="sxs-lookup"><span data-stu-id="147c9-106">This example is the **CPapFile** **Init** method from Papfile.cpp.</span></span>


```C++
HRESULT CPapFile::Init(
                      TCHAR* pszAppFileName,
                      IPaper* pIPaper)
  {
    HRESULT hr = E_FAIL;

    if (NULL != pIPaper)
    {
      // Keep CPapFile copy of pIPaper. Thus AddRef it.
      // Released in Destructor.
      m_pIPaper = pIPaper;
      m_pIPaper->AddRef();

      if (NULL != pszAppFileName)
      {
        // Set the default current file name.
        StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszAppFileName);

        hr = NOERROR;
      }
    }

    return (hr);
  }
  
```



<span data-ttu-id="147c9-107">Параметр *псзаппфиленаме* используется для инициализации кпапфиле с именем файла по умолчанию для всех последующих операций загрузки или сохранения.</span><span class="sxs-lookup"><span data-stu-id="147c9-107">The *pszAppFileName* parameter is used to initialize CPapFile with a default file name for any subsequent load or save operations.</span></span> <span data-ttu-id="147c9-108">Для первой нагрузки копия хранится в члене **m \_ сзкурфиленаме** .</span><span class="sxs-lookup"><span data-stu-id="147c9-108">A copy is kept in member **m\_szCurFileName** for the first load.</span></span> <span data-ttu-id="147c9-109">В **стоклиен** такая нагрузка предпринимается при первой загрузке приложения после инициализации Кпапфиле с *псзаппфиленаме* назначенным "стоклиен. PAP ".</span><span class="sxs-lookup"><span data-stu-id="147c9-109">In **StoClien**, such a load is attempted when the application first starts after CPapFile has been initialized with *pszAppFileName* assigned "STOCLIEN.PAP".</span></span> <span data-ttu-id="147c9-110">Это имя файла было создано в конструкторе Кгуипапер путем получения имени текущего выполняемого модуля.</span><span class="sxs-lookup"><span data-stu-id="147c9-110">This file name was constructed in a CGuiPaper constructor by obtaining the current executing module name.</span></span> <span data-ttu-id="147c9-111">(Вызывается функция Win32 [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) ).</span><span class="sxs-lookup"><span data-stu-id="147c9-111">(The Win32 [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function is called).</span></span>

<span data-ttu-id="147c9-112">Параметр *пипапер* является обязательным для кпапфиле, так как он использует этот интерфейс в объекте-документе для выполнения операций загрузки и сохранения.</span><span class="sxs-lookup"><span data-stu-id="147c9-112">The *pIPaper* parameter is required by CPapFile, because it uses this interface on the COPaper object to perform its load and save operations.</span></span> <span data-ttu-id="147c9-113">**AddRef** вызывается для этой хранимой копии *пипапер* в соответствии с правилами com.</span><span class="sxs-lookup"><span data-stu-id="147c9-113">**AddRef** is called on this stored copy of *pIPaper*, in accordance with COM rules.</span></span> <span data-ttu-id="147c9-114">Соответствующий **выпуск** вызывается в деструкторе кпапфиле.</span><span class="sxs-lookup"><span data-stu-id="147c9-114">The matching **Release** is called in the CPapFile destructor.</span></span>

 

 