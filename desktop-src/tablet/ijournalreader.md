---
description: Предоставляет доступ на чтение к файлу журнала Windows, возвращая поток, содержащий XML-версию содержимого файла.
ms.assetid: e4e19f69-6377-4f06-856d-7f9b453e7656
title: Интерфейс Ижаурналреадер (журнал. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: 7576996d341f13518879310f08c0a48996e1293f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349912"
---
# <a name="ijournalreader-interface"></a>Интерфейс Ижаурналреадер

Предоставляет доступ на чтение к файлу журнала Windows, возвращая поток, содержащий XML-версию содержимого файла.

> [!Note]  
> Компоненту чтения журнала не удается прочитать файлы журнала Windows, созданные на компьютерах под управлением Windows 7 или более поздней версии. Интерфейс Ижаурналреадер должен считаться устаревшим или устаревшим и не должен использоваться.

 

## <a name="members"></a>Элементы

Интерфейс **ижаурналреадер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Ижаурналреадер** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ижаурналреадер** содержит следующие методы.



| Метод                                                  | Описание                                                                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**реадфромстреам**](ijournalreader-readfromstream.md) | Принимает поток в файл заметки журнала и возвращает XML-поток, представляющий содержимое документа.<br/> |



 

## <a name="remarks"></a>Комментарии

Класс **жаурналреадер** позволяет загрузить поток документа журнала и получить XML-поток, представляющий содержимое. Вы можете воспроизводить, отображать и манипулировать рукописными данными.

## <a name="examples"></a>Примеры

Следующий пример обработчика для события [**нажатия**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) кнопки создает экземпляр класса **жаурналреадер** и использует его для чтения существующего файла журнала.

> [!Note]  
> Метод **дисплайксмл** , вызываемый из этого примера, не показан. Конкретная реализация такого метода зависит от потребностей вашего приложения.

 


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  static TCHAR BASED_CODE szFilter[] = 
    _T("Journal files (*.jnt)|*.jnt|All files (*.*)|*.*");
  CFileDialog* fileDialog = new CFileDialog(TRUE, _T("*.jnt"), NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user via a File Open dialog
  if (fileDialog != NULL &&
      fileDialog->DoModal() == IDOK)
  {
    CString strFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(strFileName,
                              GENERIC_READ,
                              FILE_SHARE_READ,
                              NULL,
                              OPEN_EXISTING,
                              FILE_ATTRIBUTE_NORMAL,
                              NULL);
    
    if (hFile != INVALID_HANDLE_VALUE)
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
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) &&
              (dwRead == dwFileSize))
          {
            HRESULT hr;
            IStream* pJntStream;

            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              IJournalReader* pJntReader;

              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                IStream* pXmlStream;

                // Read in the JNT file via the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                if (SUCCEEDED(hr))
                {
                  // Display results
                  DisplayXml(pXmlStream);

                  // Clean up
                  pXmlStream->Release();
                }
                pJntReader->Release();
              }
              pJntStream->Release();
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
      CloseHandle(hFile);
    }
    delete fileDialog;
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

[Идентификаторы GUID настраиваемых свойств](custom-property-guids.md)
</dt> <dt>

[**Метод Реадфромстреам**](ijournalreader-readfromstream.md)
</dt> </dl>

 

