---
title: Объявление класса Кгуипапер
description: Объявление класса Кгуипапер
ms.assetid: b772d056-bf89-46a8-9462-21772cf96dfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269694b83804f3e85cd8654cd2a1be843396a2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067505"
---
# <a name="cguipaper-class-declaration"></a>Объявление класса Кгуипапер

Ниже приведено объявление класса **кгуипапер** из Гуипапер. H.


```C++
class CGuiPaper
  {
    public:
      CGuiPaper(void);
      ~CGuiPaper(void);
      BOOL Init(HINSTANCE hInst, HWND hWnd, TCHAR* pszCmdLineFile);
      HRESULT DrawOn(void);
      HRESULT DrawOff(void);
      HRESULT ClearWin(void);
      HRESULT PaintWin(void);
      HRESULT Erase(void);
      HRESULT Resize(WORD wWidth, WORD wHeight);
      HRESULT InkWidth(SHORT nInkWidth);
      HRESULT InkColor(COLORREF crInkColor);
      HRESULT InkSaving(BOOL bInkSaving);
      HRESULT InkStart(SHORT nX, SHORT nY);
      HRESULT InkDraw(SHORT nX, SHORT nY);
      HRESULT InkStop(SHORT nX, SHORT nY);
      HRESULT ConnectPaperSink(void);
      HRESULT DisconnectPaperSink(void);
      HRESULT Load(void);
      HRESULT Save(void);
      int     AskSave(void);
      HRESULT Open(void);
      HRESULT SaveAs(void);
      COLORREF PickColor(void);

    private:
      HINSTANCE  m_hInst;
      HWND       m_hWnd;
      HDC        m_hDC;
      RECT       m_WinRect;
      IPaper*    m_pIPaper;
      SHORT      m_nLockKey;
      HPEN       m_hPen;
      SHORT      m_nInkWidth;
      COLORREF   m_crInkColor;
      BOOL       m_bInkSaving;
      BOOL       m_bInking;
      BOOL       m_bPainting;
      POINT      m_OldPos;
      IUnknown*  m_pCOPaperSink;
      DWORD      m_dwPaperSink;
      BOOL       m_bDirty;
      CPapFile*    m_pPapFile;
      OPENFILENAME m_ofnFile;
      TCHAR        m_szFileFilter[MAX_PATH];
      TCHAR        m_szFileName[MAX_PATH];
      TCHAR        m_szFileTitle[MAX_PATH];
      CHOOSECOLOR  m_ChooseColor;
      COLORREF     m_acrCustColors[16];

      IConnectionPoint* GetConnectionPoint(REFIID riid);
  };
```



**Кгуипапер** поддерживает текущие свойства графического пользовательского интерфейса для бумаги для рисования. Элементы **m \_ кринкколор**, **m \_ кринквидс** и **m \_ винрект** содержат значения для текущего цвета рукописного ввода, ширины краски и прямоугольника рисования. Элемент **m \_ HWND** сохраняет дескриптор в окне, где выполняется рисование.

Фактическое Рисование изображений выполняется с помощью маркера для контекста устройства, хранящегося в члене **m \_ HDC**. Маркер текущего пера рисования хранится в члене **m \_ Хпен**. Перо уничтожается и создается повторно при изменении его цвета или ширины пользователем.

Члены **m \_ пкопаперсинк** и **m \_ двпаперсинк** содержат значения, необходимые для подключения к сопоставлению с совместной бумагой для получения входящих уведомлений через интерфейс [**ипаперсинк**](ipapersink-methods.md) . Член **m \_ бдирти** содержит флаг, указывающий, что пользователь изменил рисунок и что он больше не отражает данные, хранящиеся в его файле.

Член **m \_ пипапер** содержит указатель основного интерфейса на объект собумаги. Доступ ко всем функциональным бумагам осуществляется через этот указатель.

Элемент **m \_ нлокккэй** используется для поддержки схемы блокировки клиента, которая используется с несколькими клиентами для обеспечения монопольного доступа клиента к совместно используемому объекту-содокументу. Собумага назначает **\_ нлокккэй m** во время вызова [**ипапер**](ipaper-methods.md)::**Lock** и передается клиентом в качестве параметра при последующих вызовах к собумагам. Собумага будет выполнять работу в этих вызовах только в том случае, если переданный ключ блокировки совпадает с ключом, который последний раз передается клиенту по сопоставлению.

Член **m \_ ппапфиле** содержит указатель на объект [**кпапфиле**](cpapfile-class-and-methods.md) . Это объект C++, инкапсулирующий операции загрузки и сохранения в структурированном составном файле хранилища. **Кпапфиле** работает с базовым трансдокументным объектом на основе сервера, чтобы загрузить и сохранить данные для рисования.

 

 




