# The Unofficial Guide

<!-- Replace this line with your name and which corpus you picked. -->

> **This file is your submission.** Fill it in as you go — most sections get
> written during the milestone that produces them, not at the end.
>
> How the starter works, and every command you'll need, is in `RUNNING.md`.
> Leave that file alone.
>
> **Paste everything as text.** No screenshots, no video. A typed table gets
> full credit; a picture of the same table gets none.
>
> Delete these instruction blocks as you replace them. The `<!-- -->` comments
> are notes to you and don't show up when the page renders — you can leave them
> or remove them.

---

# Unit 1

## What This Does

<!-- Three or four sentences. Which corpus you picked, and the kinds of
     questions your system answers. Write it for someone who has never seen
     this repo.

     Milestone 5. -->

## Chunking Strategy

**Chunk size:** 2,228 or 51 lines of text
**Overlap:** 15% of chunk size - ~335 characters of text or 8 lines of text

<!-- What about YOUR documents made you pick these numbers? Short posts and
     long sectioned guides don't want the same chunking, and "800 seemed
     reasonable" earns nothing. Point at something you noticed when you read
     the documents in Milestone 1.

     If you changed your mind partway through, say so and say why. That's worth
     more than pretending you got it right first time.

     Milestone 3. -->
     Considering the default chunk chosen for this corpus (city_guides) is 51, I chose right at 50 because it matches to the average number of "lines" of text in some of the files I've read. Each document has ranges from 35 to 51 lines of text so it is ideal. For the overlap, I checked with Claude and referenced two of the documents (`guide_brightwater.md` and `guide_seasons.md`) for how long is each subtopic paragraph compared to the whole paragraph and it is around 15% (12.5% and 20% respectively).

## Sample Chunks

<!-- Five chunks, pasted as text. Label each one and name the file it came from
     AND the function that produced it — the grader checks your code against
     what you claim here.

     `python app.py chunks -n 5` prints all three for you. Copy them straight
     across.

     Milestone 3. -->

**Chunk 1** — source: guide_accessibility.md `` — produced by: chunker.py::split_documents``

```
# Getting around the region with limited mobility

An honest assessment rather than a promotional one. Some of these places are
difficult and it is better to know in advance.

## Straightforward

**Thornby Wells** is the easiest town in the region. It is flat, compact, and
everything is within three minutes of everything else. Parking is free for two
hours anywhere in town and the station is central. The pump room and gardens
are level throughout.

**Marchwood** has a modern tram network with level boarding on all four lines,
running every 8 minutes on weekdays. The city museum and covered market are both
step-free. The distances between districts are the main consideration.

**Brightwater** is level along the river and through the centre. The mill museum
is step-free. The station is a 15-minute walk from campus on flat ground, or the
shuttle meets the four busiest arrivals.

## Mixed

**Pellew Sands** has a two-mile seafront that is flat the whole way, and
everything of interest is on it or one street back. The land train runs the
length of the promenade hourly between Easter and September. The beach itself is
hard sand and manageable at low tide.

**Givens Mill** is one flat street along the river. The mill tour involves
stairs and the machinery floor is not accessible; the tearoom and riverside are.

## Difficult

**Kestrelford** is built on a slope and the walk up from the lower car park is
steeper than it looks on a map. There is no transport within the town.

**Halden Bay** is built on three levels connected by stepped lanes. The harbour
front is level; everything above it is not. This is hard going with luggage or a
pushchair, let alone a wheelchair.

**Corry Vale** has no public transport, villages two to four miles apart, and
footpaths rather than pavements. **Elder Ness** is shingle and a single street.

## Practical

The nearest full hospital is in Marchwood. Brightwater has a hospital;
Kestrelford, Halden Bay, Corry Vale, Givens Mill and Elder Ness have minor
injuries units with limited hours or nothing at all.

Mobile coverage is good in the town centres and patchy on the outskirts, and
genuinely absent in parts of Corry Vale.
```

**Chunk 2** — source: guide_corry_vale.md `` — produced by: chunker.py::split_documents``

```
le in snow.

## Practical notes

Cash is still useful at the market and in smaller places, though cards are
accepted almost everywhere now. Mobile coverage is good in the centre and
patchy on the outskirts. The nearest full hospital is in Brightwater; there is
a minor injuries unit locally with limited hours.
```

**Chunk 3** — source: `guide_givens_mill.md` — produced by: chunker.py::split_documents``

```
# Givens Mill

Givens Mill is a village of 700 built around a working watermill that still grinds flour commercially. It is the sort of place people visit for an afternoon and then talk about for longer than the visit lasted.

## Getting there

No station and no bus on Sundays; four buses a day from Brightwater on weekdays, taking 30 minutes. Driving is 20 minutes. The village car park holds about forty cars and is full by 11am on summer Saturdays.

## Getting around

Everything is on one street along the river. The mill is at one end and the church at the other, eight minutes apart. The riverside path continues in both directions for as far as you want to walk.

## Eat and drink

A tearoom attached to the mill, open 10 to 4 daily except Tuesdays, which sells bread made from the flour ground twenty metres away and is the reason most people come. One pub, food served lunchtimes and Thursday to Saturday evenings.

## What to see

The mill runs tours on the hour from 11 to 3 and the machinery is operating during them, which is loud and much more impressive than a static exhibit. The church has a Saxon doorway. The river walk downstream reaches Brightwater in about three hours.

## Where to stay

Nothing in the village itself. The nearest rooms are in Brightwater, which is close enough that this is not really a problem — most people come for a half day.

## When to go

The mill runs March to November and is closed entirely in winter. Late spring is the best time. Summer Saturdays are busy enough that the car park becomes the limiting factor; come on a weekday if you can.

## Practical notes

Cash is still useful at the market and in smaller places, though cards are
accepted almost everywhere now. Mobile coverage is good in the centre and
patchy on the outskirts. The nearest full hospital is in Brightwater; there is
a minor injuries unit locally with limited hours.
```

**Chunk 4** — source: guide_marchwood.md `` — produced by: chunker.py::split_documents``

```
# Marchwood

Marchwood is the regional hub — 180,000 people, the junction everyone changes trains at, and a city most visitors pass through rather than stop in. That is a mistake, though an understandable one, since almost nothing of interest is near the station.

## Getting there

Every railway line in the region meets here, which is the city's defining feature. Trains to Brightwater run every 40 minutes until 11pm. The airport is 20 minutes out by a dedicated bus that runs every 15 minutes and costs more than the equivalent taxi shared between three people.

## Getting around

A tram network of four lines, running every 8 minutes on weekdays and every 15 at weekends, until midnight. A day ticket costs less than two single fares and nobody tells you this at the machine. The centre is walkable but the interesting districts are not adjacent to each other.

## Eat and drink

The best eating is in the Northgate district, a 12-minute tram ride from the station, where about thirty restaurants sit within four streets. The area immediately around the station is uniformly poor and expensive. Marchwood keeps later hours than anywhere else in the region — kitchens serve until 10:30pm, and until midnight on Fridays and Saturdays.

## What to see

The city museum is free and genuinely excellent, particularly the industrial floor. The covered market has operated since 1863 and is at its best on a weekday morning. The canal walk from Northgate to the old lock is 40 minutes and is the thing residents recommend when asked.

## Where to stay

Plentiful and, outside conference weeks, cheap. Northgate is the district worth staying in. Station-area hotels are convenient for an early train and dispiriting for anything else.

## When to go

Any time. This is the one place in the region that works in winter, since almost everything is indoors and nothing closes seasonally. Conference weeks in March and October fill the hotels and double the prices; check before booking.

## Practical notes

Cash is still useful at the market and in smaller places, though cards are
accepted almost everywhere now. Mobile coverage is good in the centre and
patchy on the outskirts. The nearest full hospital is in Brightwater; there
```

**Chunk 5** — source: guide_seasons.md `` — produced by: chunker.py::split_documents``

```
# When to visit the region

## Spring, March to May

Days lengthen quickly and businesses that closed for winter reopen through
March and April. By May everything is open and the weather is reliable enough
to plan around. Late May is arguably the best week of the year in Brightwater —
long days, everything running, and the students gone.

The Kestrelford Saturday market builds back to full size through April.

## Summer, June to August

June is excellent everywhere. July and August split: Halden Bay becomes very
busy and the parking problem dominates, Kestrelford fills with walkers, and
Brightwater goes quiet to the point of dullness with the university empty.

If you are going to Halden Bay in August, arrive before 10am or plan to use the
overflow lot.

## Autumn, September to November

September is the other sweet spot — warm, quiet, and everything still open.
From late September Brightwater is at its busiest as term starts, and
accommodation there becomes hard to find and expensive.

By November the coastal businesses begin closing and the days are short.

## Winter, December to February

Brightwater carries on, since the university keeps it occupied. Halden Bay
largely closes. Kestrelford's approach road is difficult in snow and the town
is cut off for a day or two most winters.

The coastal path is dramatic and frequently shut. Several riverside businesses
in Brightwater close entirely from January to March.
```

## Sample Answer

<!-- One complete question and answer, pasted as text, with the source line
     visible. Milestone 4. -->

**Question:** Answer using only the information in the documents below. If they don't cover it, say you don't have enough information. Document: guide_brightwater.md. What is the population of brightwater?

**Answer:** 

```
(best distance 0.499, cutoff 0.6)

Brightwater has a population of about 40,000 people, which roughly doubles during term time (guide_brightwater.md).

Sources retrieved: guide_brightwater.md, guide_corry_vale.md, guide_kestrelford.md, guide_regional_transport.md, guide_seasons.md
```

**My relevance cutoff:**

<!-- The number you set in config.py, and how you got there.

     You ran five questions your corpus covers and the five in OUT_OF_SCOPE
     that it clearly doesn't, and wrote down the best distance for each. What
     did those two groups look like? Where was the gap? Put the actual numbers
     here — the table below wants all ten rows.

     Milestone 4. -->

| Question | In corpus? | Best distance |
|---|---|---|
|What is the best place to walk in the region?|Yes|0.509|
|Which place in the region would be the best to visit in Autumn?|Yes|0.469|
|What food and drinks does Pellew Sands have?|Yes|0.541|
|What places in the region do you recommend for the someone with limited mobility to visit in the region?|Yes|0.548|
|What is the most difficult place to walk in the region?|Yes|0.548|
|Do you recommend visiting Chicago?|No|0.612|
|Who won the 1994 World Cup?|No|0.903|
|What food and drinks are in the World Cup?|No|0.753|
|What is the recommended dosage for ibuprofen for a headache?|No|0.833|
|What is the capital?|No|0.797|
|  |  |  |

## How I Used AI

<!-- Two specific moments. For each: what you asked for, what came back, and
     what you changed about it.

     "I asked Claude to write the chunking function from my notes. It ignored
     the overlap, so I added that myself" is the level of detail we're after.
     "I used AI to help me code" is not.

     Milestone 5. -->

**1.** Asked Claude to explain in more detail what "Corpus" and "Corpora" means and it did define their meanings (corpora is really just the plural of corpus) and it immediately detected that it was for a RAG pipeline and defined other useful glossary such as Chunk, Embed, and Query Time.

**2.** I used Claude to explain to me what "Chunk" and "Overlap" mean and it did define it as prompted but also recommended the overlap to be 20% of the chunk size based on usual values other RAG systems use.

<!-- ── Stretch features ─────────────────────────────────────────────────────
     Doing one? Say so here BEFORE you start. A feature this README never
     claims earns nothing.
     ───────────────────────────────────────────────────────────────────────── -->

---

# Unit 2

<!-- These sections get ADDED to what's already above. Don't delete or rewrite
     unit 1 — the point is that someone can see what you said before you knew
     how it went. -->

## Run Log — Before

<!-- Your five criteria, three runs each. `python run_eval.py --label before`
     runs the questions, puts the OUT_OF_SCOPE ones through the gate, and
     writes it all into results/ for you. Targets come from criteria.md; the
     verdict column is your call.

     Criterion 3 is measured in one deterministic pass rather than three, so
     the same number goes in all three run columns. That's correct, not lazy.

     Milestone 1. -->

| Criterion | Target | Run 1 | Run 2 | Run 3 | Verdict |
|---|---|---|---|---|---|
| 1. Retrieved chunk contains the answer | 4 of 5 |  |  |  |  |
| 2. Every answer names a source | 5 of 5 |  |  |  |  |
| 3. Gate stops out-of-corpus questions | 4 of 5 |  |  |  |  |
| 4. | | | | | |
| 5. | | | | | |

<!-- Underneath, paste the REAL output for each criterion from one of your
     runs — the actual text your system produced, not a description of it.
     Name the file and function that produced it. -->

## Verdicts

<!-- MET or MISSED for each of the five, against the target you wrote last
     unit — not a new one. Plus a sentence on how you decided. That sentence
     matters most where it was close.

     If your target said 4 of 5 and your runs came out 4, 3, 4, that's a MISS.
     The target has to hold, not show up occasionally.

     Milestone 2. -->

| # | Criterion | Verdict | How I decided |
|---|---|---|---|
| 1 |  |  |  |
| 2 |  |  |  |
| 3 |  |  |  |
| 4 |  |  |  |
| 5 |  |  |  |

## Diagnoses

<!-- For each miss: which stage caused it, and how. The stage alone isn't
     enough — you need the mechanism.

     Not a diagnosis: "Question 3 didn't work."
     A diagnosis:     "Question 3 asks about laundry costs. The answer is in
                       one sentence that got split across two chunks, so
                       neither chunk on its own contains it."

     The five stages: loading → chunking → embedding → retrieval → generation.

     Look for a pattern. If three misses all ask about numbers, that's one
     problem, not three.

     Missed nothing? Say so, then say honestly whether your targets were set
     low, and which one you'd tighten and to what.

     Milestone 3. -->

## The Improvement

**What I changed:**

**Why I picked it:**

<!-- Connect it to a specific diagnosis above in one sentence. If you can't,
     you picked a fix because it sounded impressive. -->

### Run Log — After

<!-- Same format, same five criteria, three runs each.
     `python run_eval.py --label after` -->

| Criterion | Target | Run 1 | Run 2 | Run 3 | Verdict |
|---|---|---|---|---|---|
| 1. Retrieved chunk contains the answer | 4 of 5 |  |  |  |  |
| 2. Every answer names a source | 5 of 5 |  |  |  |  |
| 3. Gate stops out-of-corpus questions | 4 of 5 |  |  |  |  |
| 4. | | | | | |
| 5. | | | | | |

**Did it help?**

<!-- Say plainly whether it did, and how you know. If it made things worse,
     say that — a change that backfired, honestly reported, earns full credit
     and is more interesting than one that worked. What matters is that you can
     tell.

     Milestone 4. -->

## What's Still Broken

<!-- For each criterion still missed after your fix: what you'd do about it,
     and why you stopped where you did.

     "I ran out of time" is fine if it's true. Pretending nothing is left is
     not.

     Milestone 5. -->

## What I'd Do Differently

<!-- Knowing what you know now — which of your five criteria would you write
     differently, and why?

     Milestone 5. -->
