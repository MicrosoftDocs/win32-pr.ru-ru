---
title: Класс и методы Кпапфиле
description: Стоклиен инкапсулирует операции с составными файлами в объекте Кпапфиле C++.
ms.assetid: 21a3e170-0a73-4744-8cfc-3a04e0571792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa970aecf275afbf7bc5b6d68c69de3367e48aa5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986350"
---
# <a name="cpapfile-class-and-methods"></a><span data-ttu-id="5c088-103">Класс и методы Кпапфиле</span><span class="sxs-lookup"><span data-stu-id="5c088-103">CPapFile Class and Methods</span></span>

<span data-ttu-id="5c088-104">**Стоклиен** инкапсулирует операции с составными файлами в объекте кпапфиле C++.</span><span class="sxs-lookup"><span data-stu-id="5c088-104">**StoClien** encapsulates its compound file operations in a CPapFile C++ object.</span></span>

<span data-ttu-id="5c088-105">Ниже приведено объявление класса **кпапфиле** из папфиле. h.</span><span class="sxs-lookup"><span data-stu-id="5c088-105">The following is the **CPapFile** class declaration from Papfile.h.</span></span>


```C++
class CPapFile
  {
    public:
      CPapFile(void);
      ~CPapFile(void);
      HRESULT Init(TCHAR* pszFileName, IPaper* pIPaper);
      HRESULT Load(SHORT nLockKey, TCHAR* pszFileName);
      HRESULT Save(SHORT nLockKey, TCHAR* pszFileName);

    private:
      TCHAR          m_szCurFileName[MAX_PATH];
      IPaper*        m_pIPaper;
      IStorage*      m_pIStorage;
  };
  
```



<span data-ttu-id="5c088-106">Объект Кпапфиле сохраняет текущее имя файла в члене **m \_ сзкурфиленаме**.</span><span class="sxs-lookup"><span data-stu-id="5c088-106">The CPapFile object keeps a current file name in member **m\_szCurFileName**.</span></span> <span data-ttu-id="5c088-107">Это имя файла используется по умолчанию в методах [**Load**](load-method---cpapfile.md) и [**Save**](save-method---cpapfile.md) , если они не получают явно имя файла.</span><span class="sxs-lookup"><span data-stu-id="5c088-107">This file name is used as a default in the [**Load**](load-method---cpapfile.md) and [**Save**](save-method---cpapfile.md) methods when they do not explicitly receive a file name.</span></span>

<span data-ttu-id="5c088-108">Член **m \_ пипапер** сохраняет указатель интерфейса на интерфейс [**ипапер**](ipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="5c088-108">Member **m\_pIPaper** keeps an interface pointer to the COPaper [**IPaper**](ipaper-methods.md) interface.</span></span> <span data-ttu-id="5c088-109">Член **m \_ пистораже** сохраняет указатель на интерфейс [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) для текущего составного файла, который **стоклиен** использует для структурированного хранилища.</span><span class="sxs-lookup"><span data-stu-id="5c088-109">Member **m\_pIStorage** keeps a pointer to the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface for the current compound file that **StoClien** is using for structured storage.</span></span>

<span data-ttu-id="5c088-110">Ниже приведена сводка методов Кпапфиле.</span><span class="sxs-lookup"><span data-stu-id="5c088-110">The following is a summary of CPapFile's methods.</span></span>


```C++
HRESULT Init(TCHAR* pszFileName, IPaper* pIPaper);
    // Initializes CPapFile.

  HRESULT Load(SHORT nLockKey, TCHAR* pszFileName);
    // Loads default or specified paper data file.

  HRESULT Save(SHORT nLockKey, TCHAR* pszFileName);
    // Saves drawing data to the current paper data file or
    // to a specified paper data file.
```



 

 




