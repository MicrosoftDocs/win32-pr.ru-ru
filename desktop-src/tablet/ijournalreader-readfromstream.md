---
description: Принимает поток в файл заметки журнала и возвращает XML-поток, представляющий содержимое документа.
ms.assetid: 5a169dfe-b102-4aef-9efe-5db2cd2fb96f
title: 'Метод Ижаурналреадер:: Реадфромстреам (журнал. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader.ReadFromStream
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: 258ac30b8857fa4ef24bd86a08c7e402229f4bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692156"
---
# <a name="ijournalreaderreadfromstream-method"></a>Метод Ижаурналреадер:: Реадфромстреам

Принимает поток в файл заметки журнала и возвращает XML-поток, представляющий содержимое документа.

> [!Note]  
> Компоненту чтения журнала не удается прочитать файлы журнала Windows, созданные на компьютерах под управлением Windows 7 или более поздней версии. Интерфейс Ижаурналреадер должен считаться устаревшим или устаревшим и не должен использоваться.

 

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ReadFromStream(
  [in]          IStream *pJournalFileStream,
  [out, retval] IStream **ppXmlStream
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пжаурналфилестреам* \[ окне\]
</dt> <dd>

Объект [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) , представляющий файл журнала для чтения.

</dd> <dt>

*ппксмлстреам* \[ out, retval\]
</dt> <dd>

Указатель на адрес объекта [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) , который получит XML-поток, созданный при чтении файла журнала.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Потоки используются для предотвращения прямого доступа к файловой системе и для выбора метода синтаксического анализа XML.

## <a name="examples"></a>Примеры

Следующий пример обработчика для события [**нажатия**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) кнопки создает экземпляр интерфейса [**интерфейса ижаурналреадер**](ijournalreader.md) и использует его для чтения существующего файла журнала.


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  IStream* pJntStream;
  IStream* pXmlStream;
  IJournalReader* pJntReader;
  HRESULT hr;
  CString szFileName = "";
  static char BASED_CODE szFilter[] = 
    "Journal files (*.jnt)|*.jnt|All files (*.*)|*.*";
  CFileDialog* fileDialog = new CFileDialog(TRUE, "*.jnt", NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user by using a File Open dialog
  if (IDOK == fileDialog->DoModal())
  {
    szFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(szFileName.GetBuffer(), GENERIC_READ, FILE_SHARE_READ, NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
    
    if (INVALID_HANDLE_VALUE != hFile)
    {
      // Allocate memory to hold the file contents
      DWORD dwFileSize = GetFileSize(hFile, NULL);
      HGLOBAL hGlobal = GlobalAlloc(GHND, dwFileSize);

      if (hGlobal != NULL)
      {
        LPBYTE pData = (LPBYTE)GlobalLock(hGlobal);

        if (pData != NULL)
        {
          DWORD dwRead;

          // Read the Journal file into the pData buffer
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) && dwRead == dwFileSize)
          {
            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                // Read in the JNT file by using the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                // Display results
                if (SUCCEEDED(hr))
                {
                  DisplayXml(pXmlStream);
                }

                // Clean up
                pXmlStream->Release();
                pJntReader = NULL;
                pJntStream->Release();
              }
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
    }
  }
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                     |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                         |
| Header<br/>                   | <dl> <dt>Журнал. h (также требуется журнал \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Journal.dll</dt> </dl>                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ижаурналреадер**](ijournalreader.md)
</dt> <dt>

[Справочник по схеме чтения журнала](journal-reader-schema-reference.md)
</dt> </dl>

 

