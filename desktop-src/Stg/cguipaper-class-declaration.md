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
# <a name="cguipaper-class-declaration"></a><span data-ttu-id="05acd-103">Объявление класса Кгуипапер</span><span class="sxs-lookup"><span data-stu-id="05acd-103">CGuiPaper Class Declaration</span></span>

<span data-ttu-id="05acd-104">Ниже приведено объявление класса **кгуипапер** из Гуипапер. H.</span><span class="sxs-lookup"><span data-stu-id="05acd-104">The following is the **CGuiPaper** class declaration from GUIPAPER.H.</span></span>


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



<span data-ttu-id="05acd-105">**Кгуипапер** поддерживает текущие свойства графического пользовательского интерфейса для бумаги для рисования.</span><span class="sxs-lookup"><span data-stu-id="05acd-105">**CGuiPaper** maintains the current GUI properties for the drawing paper.</span></span> <span data-ttu-id="05acd-106">Элементы **m \_ кринкколор**, **m \_ кринквидс** и **m \_ винрект** содержат значения для текущего цвета рукописного ввода, ширины краски и прямоугольника рисования.</span><span class="sxs-lookup"><span data-stu-id="05acd-106">Members **m\_crInkColor**, **m\_crInkWidth**, and **m\_WinRect** contain values for the current ink color, ink width, and drawing rectangle.</span></span> <span data-ttu-id="05acd-107">Элемент **m \_ HWND** сохраняет дескриптор в окне, где выполняется рисование.</span><span class="sxs-lookup"><span data-stu-id="05acd-107">The **m\_hWnd** member stores the handle to the window where painting is done.</span></span>

<span data-ttu-id="05acd-108">Фактическое Рисование изображений выполняется с помощью маркера для контекста устройства, хранящегося в члене **m \_ HDC**.</span><span class="sxs-lookup"><span data-stu-id="05acd-108">The actual painting of images is done using a handle to a device context held in member **m\_hDC**.</span></span> <span data-ttu-id="05acd-109">Маркер текущего пера рисования хранится в члене **m \_ Хпен**.</span><span class="sxs-lookup"><span data-stu-id="05acd-109">A handle to the current drawing pen is kept in member **m\_hPen**.</span></span> <span data-ttu-id="05acd-110">Перо уничтожается и создается повторно при изменении его цвета или ширины пользователем.</span><span class="sxs-lookup"><span data-stu-id="05acd-110">The pen is destroyed and recreated when its color or width is changed by the user.</span></span>

<span data-ttu-id="05acd-111">Члены **m \_ пкопаперсинк** и **m \_ двпаперсинк** содержат значения, необходимые для подключения к сопоставлению с совместной бумагой для получения входящих уведомлений через интерфейс [**ипаперсинк**](ipapersink-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="05acd-111">Members **m\_pCOPaperSink** and **m\_dwPaperSink** hold values necessary for connecting with COPaper to receive incoming notifications through the [**IPaperSink**](ipapersink-methods.md) interface.</span></span> <span data-ttu-id="05acd-112">Член **m \_ бдирти** содержит флаг, указывающий, что пользователь изменил рисунок и что он больше не отражает данные, хранящиеся в его файле.</span><span class="sxs-lookup"><span data-stu-id="05acd-112">Member **m\_bDirty** holds a flag indicating that the user has changed the drawing and that it no longer reflects the data stored in its file.</span></span>

<span data-ttu-id="05acd-113">Член **m \_ пипапер** содержит указатель основного интерфейса на объект собумаги.</span><span class="sxs-lookup"><span data-stu-id="05acd-113">Member **m\_pIPaper** holds the main interface pointer to the COPaper object.</span></span> <span data-ttu-id="05acd-114">Доступ ко всем функциональным бумагам осуществляется через этот указатель.</span><span class="sxs-lookup"><span data-stu-id="05acd-114">All of the COPaper functionality is accessed through this pointer.</span></span>

<span data-ttu-id="05acd-115">Элемент **m \_ нлокккэй** используется для поддержки схемы блокировки клиента, которая используется с несколькими клиентами для обеспечения монопольного доступа клиента к совместно используемому объекту-содокументу.</span><span class="sxs-lookup"><span data-stu-id="05acd-115">The **m\_nLockKey** member is used to support a client locking scheme that is used with multiple clients to allow a client exclusive access to a shared COPaper object.</span></span> <span data-ttu-id="05acd-116">Собумага назначает **\_ нлокккэй m** во время вызова [**ипапер**](ipaper-methods.md)::**Lock** и передается клиентом в качестве параметра при последующих вызовах к собумагам.</span><span class="sxs-lookup"><span data-stu-id="05acd-116">COPaper assigns **m\_nLockKey** during an [**IPaper**](ipaper-methods.md)::**Lock** call and is passed as a parameter by the client in subsequent calls to COPaper.</span></span> <span data-ttu-id="05acd-117">Собумага будет выполнять работу в этих вызовах только в том случае, если переданный ключ блокировки совпадает с ключом, который последний раз передается клиенту по сопоставлению.</span><span class="sxs-lookup"><span data-stu-id="05acd-117">COPaper will perform the work in those calls only if the lock key that is passed matches the key last handed out to a client by COPaper.</span></span>

<span data-ttu-id="05acd-118">Член **m \_ ппапфиле** содержит указатель на объект [**кпапфиле**](cpapfile-class-and-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="05acd-118">Member **m\_pPapFile** holds a pointer to a [**CPapFile**](cpapfile-class-and-methods.md) object.</span></span> <span data-ttu-id="05acd-119">Это объект C++, инкапсулирующий операции загрузки и сохранения в структурированном составном файле хранилища.</span><span class="sxs-lookup"><span data-stu-id="05acd-119">It is a C++ object that encapsulates load and save operations on a structured storage compound file.</span></span> <span data-ttu-id="05acd-120">**Кпапфиле** работает с базовым трансдокументным объектом на основе сервера, чтобы загрузить и сохранить данные для рисования.</span><span class="sxs-lookup"><span data-stu-id="05acd-120">**CPapFile** works with the underlying server-based COPaper object to load and save the COPaper drawing data.</span></span>

 

 




