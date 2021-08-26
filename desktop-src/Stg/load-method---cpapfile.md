---
title: Метод Load — Кпапфиле
description: После успешного выполнения этих операций полученный интерфейс IStorage освобождается. Этот файл закрывается и указывает, что файл не удерживается открытым во время других операций клиента. Он будет открыт повторно при необходимости.
ms.assetid: 40f79adb-87f3-4b0e-9cfe-927a4bc9ada5
keywords:
- Метод Load — Кпапфиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49eac23bcb79738a30b18eb87a4d8ef4598aba89de0748c58b433df28d614886
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034894"
---
# <a name="load-method---cpapfile"></a>Метод Load — Кпапфиле

После успешного выполнения этих операций полученный интерфейс [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) освобождается. Этот файл закрывается и указывает, что файл не удерживается открытым во время других операций клиента. Он будет открыт повторно при необходимости.

В этом примере используется метод **Load** **кпапфиле** из папфиле. cpp.


```C++
HRESULT CPapFile::Load(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If null file name passed then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Verify that the file is using the APPUTIL function.
    if (FileExist(pszFile))
    {
      // Use the COM service to verify that the file is actually a 
      // valid compound file.
      hr = StgIsStorageFile(pszFile);
      if (SUCCEEDED(hr))
      {
        // Use the COM service to open the compound file and
        // obtain an IStorage interface.
        hr = StgOpenStorage(
               pszFile,
               NULL,
               STGM_DIRECT | STGM_READ | STGM_SHARE_EXCLUSIVE,
               NULL,
               0,
               &m_pIStorage);
        if (SUCCEEDED(hr))
        {
          // An IStorage interface has been obtained. Now, request 
          // the COPaper object on the server side to load into  
          // itself the file's paper data using IStorage for our 
          // client-provided compound file.
          hr = m_pIPaper->Load(nLockKey, m_pIStorage);
          if (SUCCEEDED(hr))
          {
            // The paper data was loaded and a current compound
            // file name exists. Copy it for later use in a saves 
            // and loads.
            if (bNewFile)
              StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
          }

          // The Storage object is not required now. Do not hold the 
          // file open. Re-obtain the IStorage again later, when 
          // required (and thus re-open the compound file) for
          // another save or load.
          RELEASE_INTERFACE(m_pIStorage);
        }
      }
    }

    return (hr);
  }
  
```



### <a name="remarks"></a>Remarks

Как и при использовании метода [**Save**](save-method---cpapfile.md) , если для параметра *pszFileName* передается **значение NULL** , в качестве имени файла используется сохраненное содержимое члена **m \_ сзкурфиленаме** . Поскольку существующий файл может быть открыт, функция АППУТИЛ **филиксист** сначала используется для проверки существования файла. Если он существует, вызывается Стандартная функция [**стгиссторажефиле**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) Service для проверки формата файла, чтобы определить, является ли он допустимым составным файлом.

Если файл является допустимым, вызывается Стандартная функция [**стгопенстораже**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) Service, чтобы открыть файл и вернуть указатель на интерфейс [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) для него.

Первый параметр — это имя создаваемого составного файла. Как и при вызове [**стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) , эта строка ожидается в форме Юникода, и во время компиляции ANSI макрос аппутил используется для преобразования параметра ANSI в ожидаемый символ Юникода.

Второй параметр хранилища с приоритетом имеет **значение NULL**, что означает, что он не используется в этом примере.

Флаги режима доступа передаются в качестве третьего параметра, чтобы указать, какие режимы доступа разрешены для открытого файла. [**Стгм \_ READ**](stgm-constants.md) открывает файл с разрешением только для чтения. [**Стгм \_ DIRECT**](stgm-constants.md) открывает файл для прямого доступа в отличие от транзакционного доступа. [**Стгм \_ \_Монопольный доступ**](stgm-constants.md) открывает файл для монопольного использования, не являющегося общим для вызывающего.

Четвертый параметр исключения элемента в **значении NULL**, указывающий, что он не используется в этом примере.

Пятый параметр зарезервирован для будущего использования и должен быть равен нулю.

Адрес переменной указателя **m \_ пистораже** передается в качестве шестого параметра. Когда вызов завершается успешно, **m \_ пистораже** содержит указатель на интерфейс [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Это интерфейс, который используется для последующих операций с открытым файлом.

Важной операцией в этом случае является то, что объект собумага загружает данные рисования из файла. Это делается с помощью метода **Load** интерфейса [**ипапер**](ipaper-methods.md) . Если собумага завершила загрузку своих данных с помощью предоставленного [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , имя составного файла копируется в **m \_ сзкурфиленаме** в качестве нового имени текущего файла.

После успешного выполнения этих операций полученный интерфейс [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) освобождается. Этот файл закрывается и означает, что файл не удерживается открытым во время других операций клиента. Он будет открыт повторно при необходимости.

 

 




