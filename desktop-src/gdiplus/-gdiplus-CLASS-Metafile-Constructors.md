---
description: В этом разделе перечислены конструкторы класса Metafile. Полный список классов см. в разделе класс Metafile.
ms.assetid: a9648287-65d9-47d8-b32b-33f74b4fcd07
title: Конструкторы метафайлов Metafile
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9ae5fa3343aebace286591760a47a55fbbef7c9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345122"
---
# <a name="metafilemetafile-constructors"></a>Конструкторы метафайлов Metafile

В этом разделе перечислены конструкторы класса [**Metafile**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile) . Полный список классов см. в разделе **класс Metafile**.

### <a name="overload-list"></a>Список перегрузок



| Конструктор                                                                                                                                                                      | Описание                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Метафайл (WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar))                                                                                                          | Создает объект [**Metafile:: Metafile**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar)) для воспроизведения.<br/>                                                                                                                                                   |
| [**Метафайл (IStream \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream))                                                                                                          | Создает объект [**Metafile:: Metafile**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream)) из интерфейса [IStream](/windows/win32/api/objidl/nn-objidl-istream) для воспроизведения.<br/>                                                            |
| [**Метафайл (ХЕНХМЕТАФИЛЕ, BOOL)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhenhmetafile_inbool))                                                                                          | Создает объект GDI+ [**Metafile:: Metafile**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhenhmetafile_inbool)) для воспроизведения на основе файла расширенного метафайла GDI (EMF).<br/>                                                                                            |
| [**Метафайл (HDC, Емфтипе, WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inemftype_inconstwchar))                                                                         | Создает объект [**Metafile:: метафайл**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inemftype_inconstwchar)) для записи.<br/>                                                                                                                             |
| [**Метафайл (WCHAR \* , HDC, емфтипе, WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inemftype_inconstwchar))                                                        | Создает объект [**Metafile:: метафайл**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inemftype_inconstwchar)) для записи.<br/>                                                                                                                    |
| [**Метафайл (IStream \* , HDC, емфтипе, WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inemftype_inconstwchar))                                                        | Создает объект [**Metafile:: Metafile**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inemftype_inconstwchar)) для записи в интерфейс [IStream](/windows/win32/api/objidl/nn-objidl-istream) .<br/>                               |
| [**Метафайл (ХМЕТАФИЛЕ, Вмфплацеаблефилехеадер \* , bool)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhmetafile_inconstwmfplaceablefileheader_inbool))                                             | Создает объект GDI+[**Metafile:: метафайл**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhmetafile_inconstwmfplaceablefileheader_inbool)) для записи. Формат может быть размещенным метафайлом.<br/>                                                                          |
| [**Метафайл (HDC, Rect&, Метафилефрамеунит, Емфтипе, WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar))            | Создает объект [**Metafile:: метафайл**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar)) для записи.<br/>                                                                                        |
| [**Метафайл (HDC, Ректф&, Метафилефрамеунит, Емфтипе, WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar))           | Создает объект [**Metafile:: метафайл**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar)) для записи.<br/>                                                                                        |
| [**Метафайл (WCHAR \* , HDC, Rect&, метафилефрамеунит, емфтипе, WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar))    | Создает объект [**Metafile:: метафайл**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar)) для записи.<br/>                                                                                        |
| [**Метафайл (WCHAR \* , HDC, ректф&, метафилефрамеунит, емфтипе, WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar))   | Создает объект [**Metafile:: метафайл**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar)) для записи.<br/>                                                                                        |
| [**Метафайл (IStream \* , HDC, Rect&, метафилефрамеунит, емфтипе, WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar))  | Создает объект [**Metafile:: Metafile**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar)) для записи в интерфейс [IStream](/windows/win32/api/objidl/nn-objidl-istream) .<br/> |
| [**Метафайл (IStream \* , HDC, ректф&, метафилефрамеунит, емфтипе, WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar)) | Создает объект [**Metafile:: Metafile**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar)) для записи в интерфейс [IStream](/windows/win32/api/objidl/nn-objidl-istream) .<br/> |



 

 
