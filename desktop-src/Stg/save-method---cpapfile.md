---
title: Метод Save — Кпапфиле
description: При инициализации Кпапфиле его можно использовать для сохранения текущих данных, хранящихся в объекте-документе.
ms.assetid: ceac32e5-7d47-480b-b1cd-5a17ac04dd0c
keywords:
- Метод Save — Кпапфиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3166b649f28cb1a8ddc37e9efc53465a6cb5d3e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986854"
---
# <a name="save-method---cpapfile"></a>Метод Save — Кпапфиле

При инициализации **кпапфиле** его можно использовать для сохранения текущих данных, хранящихся в объекте-документе.

## <a name="save-method-papfilecpp"></a>Метод Save (ПАПФИЛЕ. CPP

В этом примере используется метод  [**Save**](ipaper--save.md) **кпапфиле** из папфиле. cpp.


```C++
HRESULT CPapFile::Save(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If a null file name is passed, then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Use the COM service to reopen, or create, the compound file.
    hr = StgCreateDocfile(
        pszFile,
    STGM_CREATE | STGM_DIRECT | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
        0,
        &m_pIStorage);
    if (SUCCEEDED(hr))
    {
      // Obtained the IStorage. The compound file is open.
      // Instruct the COPaper object on the server side to save its
      // paper data into the compound file using the IStorage of our
      // client-provided compound file.
      hr = m_pIPaper->Save(nLockKey, m_pIStorage);
      if (SUCCEEDED(hr))
      {
        // The paper data was saved and obtained a new current 
        // compound file name. Copy it for later use in saves 
        // and loads.
        if (bNewFile)
          StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
      }

      // Storage complete. Do not hold the file open.
      // Re-obtain the IStorage again later (and thus re-open
      // the compound file) when required for another save or load.
      RELEASE_INTERFACE(m_pIStorage);
    }

    return (hr);
  }
  
```



Если для параметра *pszFileName* передается **значение NULL** , в качестве имени файла используется сохраненное содержимое члена **m \_ сзкурфиленаме** . *Нлокккэй* — это ключ блокировки клиента, полученный в предыдущем вызове метода [**блокировки**](ipaper-methods.md) собумаги в интерфейсе **ипапер** .

Функция службы COM Standard [**стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) вызывается для создания составного файла, в котором будут сохранены данные рисования.

Имя создаваемого составного файла передается как первый параметр. Ожидается, что [**стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) в виде строки в Юникоде. Когда **стоклиен** компилируется для строк ANSI (Юникод не определен, что является значением по умолчанию в файле Makefile), этот вызов фактически сокращается до вызова внутренней функции аппутил, **\_ стгкреатедокфиле**. Эта функция выполняет правильное преобразование параметра Псзфиле ANSI в версию Юникода перед вызовом **стгкреатедокфиле**. Дополнительные сведения см. в разделе Аппутил. h и Stoserve.htm.

Флаги режима доступа передаются в качестве второго параметра и определяют, какие режимы доступа разрешены для нового файла. Флаг [ \_ создания](stgm-constants.md) режима доступа стгм создает новый составной файл или перезаписывает существующий с таким же именем. [Стгм \_ READWRITE](stgm-constants.md) открывает файл с разрешением на чтение и запись. [Стгм \_ DIRECT](stgm-constants.md) открывает файл для прямого доступа в отличие от транзакционного доступа. [Стгм \_ \_Монопольный доступ](stgm-constants.md) открывает файл для монопольного использования, не являющегося общим для вызывающего.

Третий параметр зарезервирован и должен быть равен нулю.

Адрес переменной указателя **m \_ пистораже** передается в [**стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) в качестве четвертого параметра. Когда вызов успешно возвращается, **m \_ пистораже** содержит указатель интерфейса на интерфейс [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Это интерфейс, который используется для последующих операций с файлом.

Важной операцией в этом случае является то, что объект собумага сохраняет данные рисования в файле. Это делается с помощью метода [**Save**](ipaper--save.md) интерфейса [**ипапер**](ipaper-methods.md) . Если относительная бумага будет сохранена в предоставленном объекте хранилища, имя составного файла будет скопировано в **\_ сзкурфиленаме m** в качестве нового имени текущего файла.

 

 




