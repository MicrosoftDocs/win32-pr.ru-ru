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
# <a name="init-method---cpapfile"></a>Метод init — Кпапфиле

В следующем примере кода показано, как инициализируется **кпапфиле** .

В этом примере используется метод  **init** **кпапфиле** из папфиле. cpp.


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



Параметр *псзаппфиленаме* используется для инициализации кпапфиле с именем файла по умолчанию для всех последующих операций загрузки или сохранения. Для первой нагрузки копия хранится в члене **m \_ сзкурфиленаме** . В **стоклиен** такая нагрузка предпринимается при первой загрузке приложения после инициализации Кпапфиле с *псзаппфиленаме* назначенным "стоклиен. PAP ". Это имя файла было создано в конструкторе Кгуипапер путем получения имени текущего выполняемого модуля. (Вызывается функция Win32 [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) ).

Параметр *пипапер* является обязательным для кпапфиле, так как он использует этот интерфейс в объекте-документе для выполнения операций загрузки и сохранения. **AddRef** вызывается для этой хранимой копии *пипапер* в соответствии с правилами com. Соответствующий **выпуск** вызывается в деструкторе кпапфиле.

 

 