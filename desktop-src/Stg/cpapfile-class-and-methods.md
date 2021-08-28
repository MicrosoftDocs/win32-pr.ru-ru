---
title: Класс и методы Кпапфиле
description: Стоклиен инкапсулирует операции с составными файлами в объекте Кпапфиле C++.
ms.assetid: 21a3e170-0a73-4744-8cfc-3a04e0571792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36eaa46b9e675be2da699ed6f2fb0e2a2d8dd6db1e25cf0afba0f216f75a59e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117962380"
---
# <a name="cpapfile-class-and-methods"></a>Класс и методы Кпапфиле

**Стоклиен** инкапсулирует операции с составными файлами в объекте кпапфиле C++.

Ниже приведено объявление класса **кпапфиле** из папфиле. h.


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



Объект Кпапфиле сохраняет текущее имя файла в члене **m \_ сзкурфиленаме**. Это имя файла используется по умолчанию в методах [**Load**](load-method---cpapfile.md) и [**Save**](save-method---cpapfile.md) , если они не получают явно имя файла.

Член **m \_ пипапер** сохраняет указатель интерфейса на интерфейс [**ипапер**](ipaper-methods.md) . Член **m \_ пистораже** сохраняет указатель на интерфейс [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) для текущего составного файла, который **стоклиен** использует для структурированного хранилища.

Ниже приведена сводка методов Кпапфиле.


```C++
HRESULT Init(TCHAR* pszFileName, IPaper* pIPaper);
    // Initializes CPapFile.

  HRESULT Load(SHORT nLockKey, TCHAR* pszFileName);
    // Loads default or specified paper data file.

  HRESULT Save(SHORT nLockKey, TCHAR* pszFileName);
    // Saves drawing data to the current paper data file or
    // to a specified paper data file.
```



 

 




